---
title: Error Code
position_number: 5
parameters:
- name:
content:
content_markdown: >-
    | HTTP Code | Response Type | Description |

    | --- | --- | --- |

    | **200** | OK | API called successfully (function execution may still fail) |

    | **400** | BAD_REQUEST | The request URL contains blacklisted keywords, or missing `validate-appkey` / `validate-timestamp` headers |

    | **403** | FORBIDDEN | Host invalid, tenant disabled, time window expired, IP not in whitelist, signature verification failed, or AppKey unauthorized |

    | **405** | METHOD_NOT_ALLOWED | Host header is null |

    | **429** | TOO_MANY_REQUESTS | Rate limit exceeded |

    | **500** | INTERNAL_SERVER_ERROR | Client IP missing, domain not found, or tenant domain info unavailable |

    | **502** | BAD_GATEWAY | Unknown error occurred |

    | **503** | SERVICE_UNAVAILABLE | Downstream service not found or temporarily unavailable |

left_code_blocks:
- code_block:
  title:
  language:
right_code_blocks:
- code_block:
  title:
  language:
---
