---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/test-azservicebusname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusName.md
ms.openlocfilehash: 0c094fbc294ac6ca5370f8d82c8ebfceac74af0a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773210"
---
# <span data-ttu-id="5c7e2-101">Test-AzServiceBusName</span><span class="sxs-lookup"><span data-stu-id="5c7e2-101">Test-AzServiceBusName</span></span>

## <span data-ttu-id="5c7e2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5c7e2-102">SYNOPSIS</span></span>
<span data-ttu-id="5c7e2-103">Verifica a disponibilidade do nome ou alias do NameSpace especificado (nome de configuração DR)</span><span class="sxs-lookup"><span data-stu-id="5c7e2-103">Checks the Availability of the given NameSpace Name or Alias (DR Configuration Name)</span></span> 

## <span data-ttu-id="5c7e2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5c7e2-104">SYNTAX</span></span>

### <span data-ttu-id="5c7e2-105">AliasCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="5c7e2-105">AliasCheckNameAvailabilitySet</span></span>
```
Test-AzServiceBusName [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5c7e2-106">NamespaceCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="5c7e2-106">NamespaceCheckNameAvailabilitySet</span></span>
```
Test-AzServiceBusName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5c7e2-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5c7e2-107">DESCRIPTION</span></span>
<span data-ttu-id="5c7e2-108">O cmdlet **Test-AzServiceBusName** verifica a disponibilidade do nome do namespace ou alias (nome de configuração de Dr)</span><span class="sxs-lookup"><span data-stu-id="5c7e2-108">The **Test-AzServiceBusName** Cmdlet Check Availability of the NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="5c7e2-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5c7e2-109">EXAMPLES</span></span>

### <span data-ttu-id="5c7e2-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5c7e2-110">Example 1</span></span>
```
PS C:\> Test-AzServiceBusName -Namespace MyNameSapceName
```

<span data-ttu-id="5c7e2-111">Retorna o status na disponibilidade do nome do namespace ' MyNameSapceName ' como verdadeiro</span><span class="sxs-lookup"><span data-stu-id="5c7e2-111">Returns the status on availability of the namespace name 'MyNameSapceName' as True</span></span>

### <span data-ttu-id="5c7e2-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="5c7e2-112">Example 2</span></span>
```
PS C:\> Test-AzServiceBusName -Namespace MyNameSapceName
```

<span data-ttu-id="5c7e2-113">Retorna o status de disponibilidade do nome do namespace ' MyNameSapceName ' como falso com motivo</span><span class="sxs-lookup"><span data-stu-id="5c7e2-113">Returns the status on availability of the namespace name 'MyNameSapceName' as False with Reason</span></span>

### <span data-ttu-id="5c7e2-114">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="5c7e2-114">Example 3</span></span>
```
PS C:\> Test-AzServiceBusName -ResourceGroupName MyResourceGroup -Namespace Test123 -AliasName myAliasName
```

## <span data-ttu-id="5c7e2-115">OS</span><span class="sxs-lookup"><span data-stu-id="5c7e2-115">PARAMETERS</span></span>

### <span data-ttu-id="5c7e2-116">-Aliasname</span><span class="sxs-lookup"><span data-stu-id="5c7e2-116">-AliasName</span></span>
<span data-ttu-id="5c7e2-117">Nome de configuração DR-nome do alias</span><span class="sxs-lookup"><span data-stu-id="5c7e2-117">DR Configuration Name - Alias Name</span></span>

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

### <span data-ttu-id="5c7e2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c7e2-118">-DefaultProfile</span></span>
<span data-ttu-id="5c7e2-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5c7e2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c7e2-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="5c7e2-120">-Namespace</span></span>
<span data-ttu-id="5c7e2-121">Nome do namespace do ServiceBus</span><span class="sxs-lookup"><span data-stu-id="5c7e2-121">Servicebus Namespace Name</span></span>

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

### <span data-ttu-id="5c7e2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c7e2-122">-ResourceGroupName</span></span>
<span data-ttu-id="5c7e2-123">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="5c7e2-123">Resource Group Name</span></span>

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

### <span data-ttu-id="5c7e2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c7e2-124">CommonParameters</span></span>
<span data-ttu-id="5c7e2-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c7e2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c7e2-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c7e2-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c7e2-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5c7e2-127">INPUTS</span></span>

### <span data-ttu-id="5c7e2-128">System. String</span><span class="sxs-lookup"><span data-stu-id="5c7e2-128">System.String</span></span>

## <span data-ttu-id="5c7e2-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5c7e2-129">OUTPUTS</span></span>

### <span data-ttu-id="5c7e2-130">Microsoft. Azure. Commands. ServiceBus. Models. PSCheckNameAvailabilityResultAttributes</span><span class="sxs-lookup"><span data-stu-id="5c7e2-130">Microsoft.Azure.Commands.ServiceBus.Models.PSCheckNameAvailabilityResultAttributes</span></span>

## <span data-ttu-id="5c7e2-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5c7e2-131">NOTES</span></span>

## <span data-ttu-id="5c7e2-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5c7e2-132">RELATED LINKS</span></span>