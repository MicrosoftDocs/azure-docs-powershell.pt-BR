---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/test-azservicebusname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusName.md
ms.openlocfilehash: a52274d44b36f2e0dea220464ba835635ab845f4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94125554"
---
# <span data-ttu-id="4ed54-101">Test-AzServiceBusName</span><span class="sxs-lookup"><span data-stu-id="4ed54-101">Test-AzServiceBusName</span></span>

## <span data-ttu-id="4ed54-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4ed54-102">SYNOPSIS</span></span>
<span data-ttu-id="4ed54-103">Verifica a disponibilidade do nome ou alias do NameSpace especificado (nome de configuração DR)</span><span class="sxs-lookup"><span data-stu-id="4ed54-103">Checks the Availability of the given NameSpace Name or Alias (DR Configuration Name)</span></span> 

## <span data-ttu-id="4ed54-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4ed54-104">SYNTAX</span></span>

### <span data-ttu-id="4ed54-105">AliasCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="4ed54-105">AliasCheckNameAvailabilitySet</span></span>
```
Test-AzServiceBusName [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4ed54-106">NamespaceCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="4ed54-106">NamespaceCheckNameAvailabilitySet</span></span>
```
Test-AzServiceBusName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ed54-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4ed54-107">DESCRIPTION</span></span>
<span data-ttu-id="4ed54-108">O cmdlet **Test-AzServiceBusName** verifica a disponibilidade do nome do namespace ou alias (nome de configuração de Dr)</span><span class="sxs-lookup"><span data-stu-id="4ed54-108">The **Test-AzServiceBusName** Cmdlet Check Availability of the NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="4ed54-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4ed54-109">EXAMPLES</span></span>

### <span data-ttu-id="4ed54-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4ed54-110">Example 1</span></span>
```
PS C:\> Test-AzServiceBusName -Namespace MyNameSapceName
```

<span data-ttu-id="4ed54-111">Retorna o status na disponibilidade do nome do namespace ' MyNameSapceName ' como verdadeiro</span><span class="sxs-lookup"><span data-stu-id="4ed54-111">Returns the status on availability of the namespace name 'MyNameSapceName' as True</span></span>

### <span data-ttu-id="4ed54-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="4ed54-112">Example 2</span></span>
```
PS C:\> Test-AzServiceBusName -Namespace MyNameSapceName
```

<span data-ttu-id="4ed54-113">Retorna o status de disponibilidade do nome do namespace ' MyNameSapceName ' como falso com motivo</span><span class="sxs-lookup"><span data-stu-id="4ed54-113">Returns the status on availability of the namespace name 'MyNameSapceName' as False with Reason</span></span>

### <span data-ttu-id="4ed54-114">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="4ed54-114">Example 3</span></span>
```
PS C:\> Test-AzServiceBusName -ResourceGroupName MyResourceGroup -Namespace Test123 -AliasName myAliasName
```

## <span data-ttu-id="4ed54-115">OS</span><span class="sxs-lookup"><span data-stu-id="4ed54-115">PARAMETERS</span></span>

### <span data-ttu-id="4ed54-116">-Aliasname</span><span class="sxs-lookup"><span data-stu-id="4ed54-116">-AliasName</span></span>
<span data-ttu-id="4ed54-117">Nome de configuração DR-nome do alias</span><span class="sxs-lookup"><span data-stu-id="4ed54-117">DR Configuration Name - Alias Name</span></span>

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

### <span data-ttu-id="4ed54-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ed54-118">-DefaultProfile</span></span>
<span data-ttu-id="4ed54-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4ed54-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ed54-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="4ed54-120">-Namespace</span></span>
<span data-ttu-id="4ed54-121">Nome do namespace do ServiceBus</span><span class="sxs-lookup"><span data-stu-id="4ed54-121">Servicebus Namespace Name</span></span>

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

### <span data-ttu-id="4ed54-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ed54-122">-ResourceGroupName</span></span>
<span data-ttu-id="4ed54-123">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="4ed54-123">Resource Group Name</span></span>

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

### <span data-ttu-id="4ed54-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ed54-124">CommonParameters</span></span>
<span data-ttu-id="4ed54-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ed54-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ed54-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ed54-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ed54-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4ed54-127">INPUTS</span></span>

### <span data-ttu-id="4ed54-128">System. String</span><span class="sxs-lookup"><span data-stu-id="4ed54-128">System.String</span></span>

## <span data-ttu-id="4ed54-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4ed54-129">OUTPUTS</span></span>

### <span data-ttu-id="4ed54-130">Microsoft. Azure. Commands. ServiceBus. Models. PSCheckNameAvailabilityResultAttributes</span><span class="sxs-lookup"><span data-stu-id="4ed54-130">Microsoft.Azure.Commands.ServiceBus.Models.PSCheckNameAvailabilityResultAttributes</span></span>

## <span data-ttu-id="4ed54-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4ed54-131">NOTES</span></span>

## <span data-ttu-id="4ed54-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4ed54-132">RELATED LINKS</span></span>
