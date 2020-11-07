---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubgeodrconfigurationbreakpair
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubGeoDRConfigurationBreakPair.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubGeoDRConfigurationBreakPair.md
ms.openlocfilehash: 26bbf8e86b1a7f9c4c1951a8bf2b284f8740bd74
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93777513"
---
# <span data-ttu-id="d4990-101">Set-AzEventHubGeoDRConfigurationBreakPair</span><span class="sxs-lookup"><span data-stu-id="d4990-101">Set-AzEventHubGeoDRConfigurationBreakPair</span></span>

## <span data-ttu-id="d4990-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d4990-102">SYNOPSIS</span></span>
<span data-ttu-id="d4990-103">Esta operação desabilita a recuperação de desastres e interrompe a replicação de alterações de namespaces primário para secundário</span><span class="sxs-lookup"><span data-stu-id="d4990-103">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="d4990-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d4990-104">SYNTAX</span></span>

### <span data-ttu-id="d4990-105">GeoDRParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="d4990-105">GeoDRParameterSet (Default)</span></span>
```
Set-AzEventHubGeoDRConfigurationBreakPair [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4990-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d4990-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzEventHubGeoDRConfigurationBreakPair [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4990-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4990-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzEventHubGeoDRConfigurationBreakPair [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4990-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d4990-108">DESCRIPTION</span></span>
<span data-ttu-id="d4990-109">O cmdlet **set-AzEventHubGeoDRConfigurationBreakPair** desabilita a recuperação de desastres e interrompe a replicação de alterações de namespaces primário para secundário</span><span class="sxs-lookup"><span data-stu-id="d4990-109">The **Set-AzEventHubGeoDRConfigurationBreakPair** cmdlet disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="d4990-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d4990-110">EXAMPLES</span></span>

### <span data-ttu-id="d4990-111">Exemplo</span><span class="sxs-lookup"><span data-stu-id="d4990-111">Example</span></span>
```
PS C:\> Set-AzEventHubGeoDRConfigurationBreakPair -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName"
```

<span data-ttu-id="d4990-112">Esta operação desabilita a recuperação de desastres e interrompe a replicação de alterações de namespaces primário para secundário</span><span class="sxs-lookup"><span data-stu-id="d4990-112">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="d4990-113">OS</span><span class="sxs-lookup"><span data-stu-id="d4990-113">PARAMETERS</span></span>

### <span data-ttu-id="d4990-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4990-114">-DefaultProfile</span></span>
<span data-ttu-id="d4990-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d4990-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4990-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d4990-116">-InputObject</span></span>
<span data-ttu-id="d4990-117">Objeto de configuração GeoDR do Eventhub</span><span class="sxs-lookup"><span data-stu-id="d4990-117">Eventhub GeoDR Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes
Parameter Sets: GeoDRConfigurationInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d4990-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="d4990-118">-Name</span></span>
<span data-ttu-id="d4990-119">Nome de configuração DR</span><span class="sxs-lookup"><span data-stu-id="d4990-119">DR Configuration Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4990-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d4990-120">-Namespace</span></span>
<span data-ttu-id="d4990-121">Nome do namespace-namespace primário</span><span class="sxs-lookup"><span data-stu-id="d4990-121">Namespace Name - Primary Namespace</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4990-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d4990-122">-PassThru</span></span>
<span data-ttu-id="d4990-123">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="d4990-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d4990-124">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="d4990-124">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4990-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4990-125">-ResourceGroupName</span></span>
<span data-ttu-id="d4990-126">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="d4990-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4990-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d4990-127">-ResourceId</span></span>
<span data-ttu-id="d4990-128">ID do recurso GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="d4990-128">GeoDRConfiguration Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRConfigResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4990-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d4990-129">-Confirm</span></span>
<span data-ttu-id="d4990-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4990-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4990-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4990-131">-WhatIf</span></span>
<span data-ttu-id="d4990-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d4990-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4990-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d4990-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4990-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4990-134">CommonParameters</span></span>
<span data-ttu-id="d4990-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4990-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4990-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4990-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4990-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d4990-137">INPUTS</span></span>

### <span data-ttu-id="d4990-138">System. String</span><span class="sxs-lookup"><span data-stu-id="d4990-138">System.String</span></span>

### <span data-ttu-id="d4990-139">Microsoft. Azure. Commands. EventHub. Models. PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="d4990-139">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="d4990-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d4990-140">OUTPUTS</span></span>

### <span data-ttu-id="d4990-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d4990-141">System.Boolean</span></span>

## <span data-ttu-id="d4990-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d4990-142">NOTES</span></span>

## <span data-ttu-id="d4990-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d4990-143">RELATED LINKS</span></span>
