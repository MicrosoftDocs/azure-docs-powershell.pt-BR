---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/test-azeventhubname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Test-AzEventHubName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Test-AzEventHubName.md
ms.openlocfilehash: 6620579ad49143dc715fc62f23d305e2efd3d5ed
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892638"
---
# <span data-ttu-id="34879-101">Test-AzEventHubName</span><span class="sxs-lookup"><span data-stu-id="34879-101">Test-AzEventHubName</span></span>

## <span data-ttu-id="34879-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34879-102">SYNOPSIS</span></span>
<span data-ttu-id="34879-103">Verifica a disponibilidade do nome ou alias do NameSpace ou alias (nome de configuração do DR)</span><span class="sxs-lookup"><span data-stu-id="34879-103">Checks the Availability of the given NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="34879-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="34879-104">SYNTAX</span></span>

### <span data-ttu-id="34879-105">NamespaceCheckNameAvailabilitySet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="34879-105">NamespaceCheckNameAvailabilitySet (Default)</span></span>
```
Test-AzEventHubName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="34879-106">AliasCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="34879-106">AliasCheckNameAvailabilitySet</span></span>
```
Test-AzEventHubName [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34879-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="34879-107">DESCRIPTION</span></span>
<span data-ttu-id="34879-108">O cmdlet **Test-AzEventhubName** Check Availability of the NameSpace Name or Alias (DR Configuration Name)</span><span class="sxs-lookup"><span data-stu-id="34879-108">The **Test-AzEventhubName** Cmdlet Check Availability of the NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="34879-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="34879-109">EXAMPLES</span></span>

### <span data-ttu-id="34879-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="34879-110">Example 1</span></span>
```
PS C:\> Test-AzEventhubName -Namespace MyNameSapceName
```

<span data-ttu-id="34879-111">Retorna o status sobre a disponibilidade do nome do namespace 'MyNameSapceName' como True, se disponível</span><span class="sxs-lookup"><span data-stu-id="34879-111">Returns the status on availability of the namespace name 'MyNameSapceName' as True if available</span></span>

### <span data-ttu-id="34879-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="34879-112">Example 2</span></span>
```
PS C:\> Test-AzEventhubName -Namespace MyNameSapceName
```

<span data-ttu-id="34879-113">Retorna o status sobre a disponibilidade do nome do namespace 'MyNameSapceName' como False com Motivo</span><span class="sxs-lookup"><span data-stu-id="34879-113">Returns the status on availability of the namespace name 'MyNameSapceName' as False with Reason</span></span>

### <span data-ttu-id="34879-114">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="34879-114">Example 3</span></span>
```
PS C:\> Test-AzEventhubName -ResourceGroupName MyResourceGroup -Namespace Test123 -AliasName myAliasName
```

<span data-ttu-id="34879-115">Retorna o status sobre a disponibilidade do nome de alias 'myAliasName' para namespace 'MyNameSapceName' como True, se disponível</span><span class="sxs-lookup"><span data-stu-id="34879-115">Returns the status on availability of the alias name 'myAliasName' for namespace 'MyNameSapceName' as True if available</span></span>

## <span data-ttu-id="34879-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="34879-116">PARAMETERS</span></span>

### <span data-ttu-id="34879-117">-AliasName</span><span class="sxs-lookup"><span data-stu-id="34879-117">-AliasName</span></span>
<span data-ttu-id="34879-118">Nome da configuração dr - Nome do alias</span><span class="sxs-lookup"><span data-stu-id="34879-118">DR Configuration Name - Alias Name</span></span>

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

### <span data-ttu-id="34879-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34879-119">-DefaultProfile</span></span>
<span data-ttu-id="34879-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="34879-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34879-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="34879-121">-Namespace</span></span>
<span data-ttu-id="34879-122">Nome do Namespace Eventhub</span><span class="sxs-lookup"><span data-stu-id="34879-122">Eventhub Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34879-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34879-123">-ResourceGroupName</span></span>
<span data-ttu-id="34879-124">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="34879-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34879-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34879-125">CommonParameters</span></span>
<span data-ttu-id="34879-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34879-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34879-127">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34879-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34879-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="34879-128">INPUTS</span></span>

### <span data-ttu-id="34879-129">System.String</span><span class="sxs-lookup"><span data-stu-id="34879-129">System.String</span></span>

## <span data-ttu-id="34879-130">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="34879-130">OUTPUTS</span></span>

### <span data-ttu-id="34879-131">Microsoft.Azure.Commands.EventHub.Models.PSCheckNameAvailabilityResultAttributes</span><span class="sxs-lookup"><span data-stu-id="34879-131">Microsoft.Azure.Commands.EventHub.Models.PSCheckNameAvailabilityResultAttributes</span></span>

## <span data-ttu-id="34879-132">NOTES</span><span class="sxs-lookup"><span data-stu-id="34879-132">NOTES</span></span>

## <span data-ttu-id="34879-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="34879-133">RELATED LINKS</span></span>
