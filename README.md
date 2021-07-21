# tailwind-accordion-test

```javascript
              <Disclosure key={key}>
                {({ open }) => (
                  <>
                    <Disclosure.Button className="flex justify-start w-full py-8 text-4xl font-medium text-left rounded-lg focus:outline-none focus-visible:ring focus-visible:ring-purple-500 focus-visible:ring-opacity-75">
                      <ChevronRightIcon
                        className={`${
                          open ? "transform rotate-90" : ""
                        } w-8 h-8 text-htx-red`}
                      />{" "}
                      <span>{navItem.navMenuLabel}</span>
                    </Disclosure.Button>
                    <Disclosure.Panel
                      className="px-4 pt-4 pb-2 text-sm"
                      key={key}
                    >
                      <Transition
                        enter="transition duration-100 ease-out"
                        enterFrom="transform scale-95 opacity-0"
                        enterTo="transform scale-100 opacity-100"
                        leave="transition duration-75 ease-out"
                        leaveFrom="transform scale-100 opacity-100"
                        leaveTo="transform scale-95 opacity-0"
                      >
                        <div className="items-center justify-between py-14 px-5">
                          <div className="mb-14">
                            <p className="text-2xl font-semibold">
                              {navItem.blurb}
                            </p>
                          </div>
                          <div className="mb-14">
                            <Link href={navItem.ctaButton.url}>
                              <a className="bg-htx-blue text-white text-2xl rounded-full ml-8 py-3 px-6">
                                {navItem.ctaButton.label}
                              </a>
                            </Link>
                          </div>
                        </div>
                        <NavMenuContent sidemenus={navItem.sidemenus} />
                      </Transition>
                    </Disclosure.Panel>
```
