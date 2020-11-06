---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/test-azurermservicebusname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Test-AzureRmServiceBusName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Test-AzureRmServiceBusName.md
ms.openlocfilehash: e7fafeeee8a377cc9bb7eb9ce514c0a0d7b89c9f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429329"
---
# <span data-ttu-id="2ffb7-101">Test-AzureRmServiceBusName</span><span class="sxs-lookup"><span data-stu-id="2ffb7-101">Test-AzureRmServiceBusName</span></span>

## <span data-ttu-id="2ffb7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2ffb7-102">SYNOPSIS</span></span>
<span data-ttu-id="2ffb7-103">Verifica a disponibilidade do nome ou alias do NameSpace especificado (nome de configuração DR)</span><span class="sxs-lookup"><span data-stu-id="2ffb7-103">Checks the Availability of the given NameSpace Name or Alias (DR Configuration Name)</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ffb7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2ffb7-104">SYNTAX</span></span>

### <span data-ttu-id="2ffb7-105">AliasCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="2ffb7-105">AliasCheckNameAvailabilitySet</span></span>
```
Test-AzureRmServiceBusName [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2ffb7-106">NamespaceCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="2ffb7-106">NamespaceCheckNameAvailabilitySet</span></span>
```
Test-AzureRmServiceBusName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2ffb7-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2ffb7-107">DESCRIPTION</span></span>
<span data-ttu-id="2ffb7-108">O cmdlet **Test-AzureRmServiceBusName** verifica a disponibilidade do nome do namespace ou alias (nome de configuração de Dr)</span><span class="sxs-lookup"><span data-stu-id="2ffb7-108">The **Test-AzureRmServiceBusName** Cmdlet Check Availability of the NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="2ffb7-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2ffb7-109">EXAMPLES</span></span>

### <span data-ttu-id="2ffb7-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2ffb7-110">Example 1</span></span>
```
PS C:\> Test-AzureRmServiceBusName -Namespace MyNameSapceName
```

<span data-ttu-id="2ffb7-111">Retorna o status na disponibilidade do nome do namespace ' MyNameSapceName ' como verdadeiro</span><span class="sxs-lookup"><span data-stu-id="2ffb7-111">Returns the status on availability of the namespace name 'MyNameSapceName' as True</span></span>

### <span data-ttu-id="2ffb7-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="2ffb7-112">Example 2</span></span>
```
PS C:\> Test-AzureRmServiceBusName -Namespace MyNameSapceName
```

<span data-ttu-id="2ffb7-113">Retorna o status de disponibilidade do nome do namespace ' MyNameSapceName ' como falso com motivo</span><span class="sxs-lookup"><span data-stu-id="2ffb7-113">Returns the status on availability of the namespace name 'MyNameSapceName' as False with Reason</span></span>

### <span data-ttu-id="2ffb7-114">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="2ffb7-114">Example 3</span></span>
```
PS C:\> Test-AzureRmServiceBusName -ResourceGroupName MyResourceGroup -Namespace Test123 -AliasName myAliasName
```

## <span data-ttu-id="2ffb7-115">OS</span><span class="sxs-lookup"><span data-stu-id="2ffb7-115">PARAMETERS</span></span>

### <span data-ttu-id="2ffb7-116">-Aliasname</span><span class="sxs-lookup"><span data-stu-id="2ffb7-116">-AliasName</span></span>
<span data-ttu-id="2ffb7-117">Nome de configuração DR-nome do alias</span><span class="sxs-lookup"><span data-stu-id="2ffb7-117">DR Configuration Name - Alias Name</span></span>

```yaml
Type: System.String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ffb7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ffb7-118">-DefaultProfile</span></span>
<span data-ttu-id="2ffb7-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2ffb7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ffb7-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="2ffb7-120">-Namespace</span></span>
<span data-ttu-id="2ffb7-121">Nome do namespace do ServiceBus</span><span class="sxs-lookup"><span data-stu-id="2ffb7-121">Servicebus Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ffb7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ffb7-122">-ResourceGroupName</span></span>
<span data-ttu-id="2ffb7-123">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="2ffb7-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ffb7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ffb7-124">CommonParameters</span></span>
<span data-ttu-id="2ffb7-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ffb7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ffb7-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ffb7-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ffb7-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2ffb7-127">INPUTS</span></span>

### <span data-ttu-id="2ffb7-128">System. String</span><span class="sxs-lookup"><span data-stu-id="2ffb7-128">System.String</span></span>

## <span data-ttu-id="2ffb7-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2ffb7-129">OUTPUTS</span></span>

### <span data-ttu-id="2ffb7-130">Microsoft. Azure. Commands. ServiceBus. Models. PSCheckNameAvailabilityResultAttributes</span><span class="sxs-lookup"><span data-stu-id="2ffb7-130">Microsoft.Azure.Commands.ServiceBus.Models.PSCheckNameAvailabilityResultAttributes</span></span>

## <span data-ttu-id="2ffb7-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2ffb7-131">NOTES</span></span>

## <span data-ttu-id="2ffb7-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2ffb7-132">RELATED LINKS</span></span>