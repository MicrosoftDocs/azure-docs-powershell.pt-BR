---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/test-azservicebusname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusName.md
ms.openlocfilehash: b2bca900be878e6f89f52b1f6096e82f79ec7863
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886584"
---
# <span data-ttu-id="e1557-101">Test-AzServiceBusName</span><span class="sxs-lookup"><span data-stu-id="e1557-101">Test-AzServiceBusName</span></span>

## <span data-ttu-id="e1557-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1557-102">SYNOPSIS</span></span>
<span data-ttu-id="e1557-103">Verifica a disponibilidade do nome ou alias do NameSpace ou alias (nome de configuração do DR)</span><span class="sxs-lookup"><span data-stu-id="e1557-103">Checks the Availability of the given NameSpace Name or Alias (DR Configuration Name)</span></span> 

## <span data-ttu-id="e1557-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e1557-104">SYNTAX</span></span>

### <span data-ttu-id="e1557-105">AliasCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="e1557-105">AliasCheckNameAvailabilitySet</span></span>
```
Test-AzServiceBusName [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1557-106">NamespaceCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="e1557-106">NamespaceCheckNameAvailabilitySet</span></span>
```
Test-AzServiceBusName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1557-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e1557-107">DESCRIPTION</span></span>
<span data-ttu-id="e1557-108">O **cmdlet Test-AzServiceBusName** Check Availability of the NameSpace Name or Alias (DR Configuration Name)</span><span class="sxs-lookup"><span data-stu-id="e1557-108">The **Test-AzServiceBusName** Cmdlet Check Availability of the NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="e1557-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e1557-109">EXAMPLES</span></span>

### <span data-ttu-id="e1557-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e1557-110">Example 1</span></span>
```
PS C:\> Test-AzServiceBusName -Namespace MyNameSapceName
```

<span data-ttu-id="e1557-111">Retorna o status sobre a disponibilidade do nome do namespace 'MyNameSapceName' como True</span><span class="sxs-lookup"><span data-stu-id="e1557-111">Returns the status on availability of the namespace name 'MyNameSapceName' as True</span></span>

### <span data-ttu-id="e1557-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e1557-112">Example 2</span></span>
```
PS C:\> Test-AzServiceBusName -Namespace MyNameSapceName
```

<span data-ttu-id="e1557-113">Retorna o status sobre a disponibilidade do nome do namespace 'MyNameSapceName' como False com Motivo</span><span class="sxs-lookup"><span data-stu-id="e1557-113">Returns the status on availability of the namespace name 'MyNameSapceName' as False with Reason</span></span>

### <span data-ttu-id="e1557-114">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="e1557-114">Example 3</span></span>
```
PS C:\> Test-AzServiceBusName -ResourceGroupName MyResourceGroup -Namespace Test123 -AliasName myAliasName
```

## <span data-ttu-id="e1557-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e1557-115">PARAMETERS</span></span>

### <span data-ttu-id="e1557-116">-AliasName</span><span class="sxs-lookup"><span data-stu-id="e1557-116">-AliasName</span></span>
<span data-ttu-id="e1557-117">Nome da configuração dr - Nome do alias</span><span class="sxs-lookup"><span data-stu-id="e1557-117">DR Configuration Name - Alias Name</span></span>

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

### <span data-ttu-id="e1557-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1557-118">-DefaultProfile</span></span>
<span data-ttu-id="e1557-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e1557-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1557-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e1557-120">-Namespace</span></span>
<span data-ttu-id="e1557-121">Nome do Namespace servicebus</span><span class="sxs-lookup"><span data-stu-id="e1557-121">Servicebus Namespace Name</span></span>

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

### <span data-ttu-id="e1557-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1557-122">-ResourceGroupName</span></span>
<span data-ttu-id="e1557-123">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="e1557-123">Resource Group Name</span></span>

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

### <span data-ttu-id="e1557-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1557-124">CommonParameters</span></span>
<span data-ttu-id="e1557-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1557-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1557-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1557-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1557-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e1557-127">INPUTS</span></span>

### <span data-ttu-id="e1557-128">System.String</span><span class="sxs-lookup"><span data-stu-id="e1557-128">System.String</span></span>

## <span data-ttu-id="e1557-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e1557-129">OUTPUTS</span></span>

### <span data-ttu-id="e1557-130">Microsoft.Azure.Commands.ServiceBus.Models.PSCheckNameAvailabilityResultAttributes</span><span class="sxs-lookup"><span data-stu-id="e1557-130">Microsoft.Azure.Commands.ServiceBus.Models.PSCheckNameAvailabilityResultAttributes</span></span>

## <span data-ttu-id="e1557-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="e1557-131">NOTES</span></span>

## <span data-ttu-id="e1557-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e1557-132">RELATED LINKS</span></span>
