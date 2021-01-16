---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubgeodrconfigurationbreakpair
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubGeoDRConfigurationBreakPair.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubGeoDRConfigurationBreakPair.md
ms.openlocfilehash: f343b92452a34a746d9ff09d5a519519aeaa7a6c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258141"
---
# <span data-ttu-id="a15bd-101">Set-AzEventHubGeoDRConfigurationBreakPair</span><span class="sxs-lookup"><span data-stu-id="a15bd-101">Set-AzEventHubGeoDRConfigurationBreakPair</span></span>

## <span data-ttu-id="a15bd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a15bd-102">SYNOPSIS</span></span>
<span data-ttu-id="a15bd-103">Esta operação desabilita a recuperação de desastres e interrompe a replicação de alterações de namespaces primário para secundário</span><span class="sxs-lookup"><span data-stu-id="a15bd-103">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="a15bd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a15bd-104">SYNTAX</span></span>

### <span data-ttu-id="a15bd-105">GeoDRParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="a15bd-105">GeoDRParameterSet (Default)</span></span>
```
Set-AzEventHubGeoDRConfigurationBreakPair [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a15bd-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a15bd-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzEventHubGeoDRConfigurationBreakPair [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a15bd-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a15bd-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzEventHubGeoDRConfigurationBreakPair [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a15bd-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a15bd-108">DESCRIPTION</span></span>
<span data-ttu-id="a15bd-109">O cmdlet **set-AzEventHubGeoDRConfigurationBreakPair** desabilita a recuperação de desastres e interrompe a replicação de alterações de namespaces primário para secundário</span><span class="sxs-lookup"><span data-stu-id="a15bd-109">The **Set-AzEventHubGeoDRConfigurationBreakPair** cmdlet disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="a15bd-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a15bd-110">EXAMPLES</span></span>

### <span data-ttu-id="a15bd-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a15bd-111">Example 1</span></span>
```powershell
PS C:\> Set-AzEventHubGeoDRConfigurationBreakPair -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName"
```

<span data-ttu-id="a15bd-112">Esta operação desabilita a recuperação de desastres e interrompe a replicação de alterações de namespaces primário para secundário</span><span class="sxs-lookup"><span data-stu-id="a15bd-112">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="a15bd-113">OS</span><span class="sxs-lookup"><span data-stu-id="a15bd-113">PARAMETERS</span></span>

### <span data-ttu-id="a15bd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a15bd-114">-DefaultProfile</span></span>
<span data-ttu-id="a15bd-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a15bd-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a15bd-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a15bd-116">-InputObject</span></span>
<span data-ttu-id="a15bd-117">Objeto de configuração GeoDR do Eventhub</span><span class="sxs-lookup"><span data-stu-id="a15bd-117">Eventhub GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="a15bd-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="a15bd-118">-Name</span></span>
<span data-ttu-id="a15bd-119">Nome de configuração DR</span><span class="sxs-lookup"><span data-stu-id="a15bd-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="a15bd-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="a15bd-120">-Namespace</span></span>
<span data-ttu-id="a15bd-121">Nome do namespace-namespace primário</span><span class="sxs-lookup"><span data-stu-id="a15bd-121">Namespace Name - Primary Namespace</span></span>

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

### <span data-ttu-id="a15bd-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a15bd-122">-PassThru</span></span>
<span data-ttu-id="a15bd-123">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="a15bd-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a15bd-124">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="a15bd-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a15bd-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a15bd-125">-ResourceGroupName</span></span>
<span data-ttu-id="a15bd-126">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="a15bd-126">Resource Group Name</span></span>

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

### <span data-ttu-id="a15bd-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a15bd-127">-ResourceId</span></span>
<span data-ttu-id="a15bd-128">ID do recurso GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="a15bd-128">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="a15bd-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a15bd-129">-Confirm</span></span>
<span data-ttu-id="a15bd-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a15bd-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a15bd-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a15bd-131">-WhatIf</span></span>
<span data-ttu-id="a15bd-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a15bd-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a15bd-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a15bd-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a15bd-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a15bd-134">CommonParameters</span></span>
<span data-ttu-id="a15bd-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a15bd-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a15bd-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a15bd-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a15bd-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a15bd-137">INPUTS</span></span>

### <span data-ttu-id="a15bd-138">System. String</span><span class="sxs-lookup"><span data-stu-id="a15bd-138">System.String</span></span>

### <span data-ttu-id="a15bd-139">Microsoft. Azure. Commands. EventHub. Models. PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="a15bd-139">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="a15bd-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a15bd-140">OUTPUTS</span></span>

### <span data-ttu-id="a15bd-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a15bd-141">System.Boolean</span></span>

## <span data-ttu-id="a15bd-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a15bd-142">NOTES</span></span>

## <span data-ttu-id="a15bd-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a15bd-143">RELATED LINKS</span></span>
