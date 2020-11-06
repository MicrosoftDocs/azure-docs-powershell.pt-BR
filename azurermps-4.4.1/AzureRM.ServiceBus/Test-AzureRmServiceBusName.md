---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Test-AzureRmServiceBusName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Test-AzureRmServiceBusName.md
ms.openlocfilehash: 892177efebb3a62e40f79b80b1ac67c488e048d9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610167"
---
# <span data-ttu-id="6233d-101">Test-AzureRmServiceBusName</span><span class="sxs-lookup"><span data-stu-id="6233d-101">Test-AzureRmServiceBusName</span></span>

## <span data-ttu-id="6233d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6233d-102">SYNOPSIS</span></span>
<span data-ttu-id="6233d-103">Verifica a disponibilidade do nome do NameSpace especificado</span><span class="sxs-lookup"><span data-stu-id="6233d-103">Checks the Availability of the given NameSpace Name</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6233d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6233d-104">SYNTAX</span></span>

```
Test-AzureRmServiceBusName [-Namespace] <String>
```

## <span data-ttu-id="6233d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6233d-105">DESCRIPTION</span></span>
<span data-ttu-id="6233d-106">O cmdlet **Test-AzureRmServiceBusName** verifica a disponibilidade do nome do namespace</span><span class="sxs-lookup"><span data-stu-id="6233d-106">The **Test-AzureRmServiceBusName** Cmdlet Check Availability of the NameSpace Name</span></span>

## <span data-ttu-id="6233d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6233d-107">EXAMPLES</span></span>

### <span data-ttu-id="6233d-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6233d-108">Example 1</span></span>
```
PS C:\> Test-AzureRmServiceBusName -Namespace TestingtheAvailability
```

### <span data-ttu-id="6233d-109">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="6233d-109">Example 2</span></span>
```
PS C:\> Test-AzureRmServiceBusName -Namespace Testi
```

### <span data-ttu-id="6233d-110">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="6233d-110">Example 3</span></span>
```
PS C:\> Test-AzureRmServiceBusName -Namespace Test123
```

<span data-ttu-id="6233d-111">Retorna o status na disponibilidade do nome do namespace</span><span class="sxs-lookup"><span data-stu-id="6233d-111">Returns the status on availability of the namespace name</span></span>

## <span data-ttu-id="6233d-112">OS</span><span class="sxs-lookup"><span data-stu-id="6233d-112">PARAMETERS</span></span>

### <span data-ttu-id="6233d-113">-Namespace</span><span class="sxs-lookup"><span data-stu-id="6233d-113">-Namespace</span></span>
<span data-ttu-id="6233d-114">Nome do namespace do ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="6233d-114">ServiceBus Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```
### <span data-ttu-id="6233d-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6233d-115">CommonParameters</span></span>
<span data-ttu-id="6233d-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6233d-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6233d-117">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6233d-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6233d-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6233d-118">INPUTS</span></span>

### <span data-ttu-id="6233d-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="6233d-119">-Namespace</span></span>
 <span data-ttu-id="6233d-120">System. String</span><span class="sxs-lookup"><span data-stu-id="6233d-120">System.String</span></span>

## <span data-ttu-id="6233d-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6233d-121">OUTPUTS</span></span>

### <span data-ttu-id="6233d-122">[Microsoft. Azure. Commands. ServiceBus. Models. CheckNameAvailabilityResultAttributes, Microsoft. Azure. Commands. ServiceBus, Version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]</span><span class="sxs-lookup"><span data-stu-id="6233d-122">[Microsoft.Azure.Commands.ServiceBus.Models.CheckNameAvailabilityResultAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]</span></span>

### <span data-ttu-id="6233d-123">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6233d-123">Example 1</span></span>
<span data-ttu-id="6233d-124">Mensagem do motivo NameAvailable</span><span class="sxs-lookup"><span data-stu-id="6233d-124">NameAvailable Reason Message</span></span>
------------- ------ -------
         True   None

### <span data-ttu-id="6233d-125">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="6233d-125">Example 2</span></span>
<span data-ttu-id="6233d-126">Mensagem do motivo NameAvailable</span><span class="sxs-lookup"><span data-stu-id="6233d-126">NameAvailable      Reason Message</span></span>
-------------      ------ -------
        False InvalidName The specified service namespace is invalid.

### <span data-ttu-id="6233d-127">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="6233d-127">Example 3</span></span>
<span data-ttu-id="6233d-128">Mensagem do motivo NameAvailable</span><span class="sxs-lookup"><span data-stu-id="6233d-128">NameAvailable    Reason Message</span></span>
-------------    ------ -------
        False NameInUse The specified service namespace is not available.

## <span data-ttu-id="6233d-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6233d-129">NOTES</span></span>

## <span data-ttu-id="6233d-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6233d-130">RELATED LINKS</span></span>
