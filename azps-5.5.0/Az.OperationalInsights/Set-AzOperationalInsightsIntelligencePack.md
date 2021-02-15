---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 23ED4D24-66BD-46E9-BB57-6E0DA679B733
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightsintelligencepack
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsIntelligencePack.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsIntelligencePack.md
ms.openlocfilehash: a8d799cec6278149cb4c08faf68584fb7968f85e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111522"
---
# <span data-ttu-id="fef95-101">Set-AzOperationalInsightsIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="fef95-101">Set-AzOperationalInsightsIntelligencePack</span></span>

## <span data-ttu-id="fef95-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fef95-102">SYNOPSIS</span></span>
<span data-ttu-id="fef95-103">Habilita ou desabilita o Pacote de Inteligência especificado.</span><span class="sxs-lookup"><span data-stu-id="fef95-103">Enables or disables the specified Intelligence Pack.</span></span>

## <span data-ttu-id="fef95-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fef95-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsIntelligencePack [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-IntelligencePackName] <String> [-Enabled] <Boolean> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fef95-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="fef95-105">DESCRIPTION</span></span>
<span data-ttu-id="fef95-106">O cmdlet **Set-AzOperationalInsightsIntelligencePack** habilita o  Pacote de Inteligência especificado se Habilitado  estiver definido como $True e desabilitá-lo se Habilitado estiver definido como $False.</span><span class="sxs-lookup"><span data-stu-id="fef95-106">The **Set-AzOperationalInsightsIntelligencePack** cmdlet enables the specified Intelligence Pack if *Enabled* is set to $True and disables it if *Enabled* is set to $False.</span></span>

## <span data-ttu-id="fef95-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fef95-107">EXAMPLES</span></span>

### <span data-ttu-id="fef95-108">Exemplo 1: Definir Pacotes de Inteligência</span><span class="sxs-lookup"><span data-stu-id="fef95-108">Example 1: Set Intelligence Packs</span></span>
```
PS C:\>Set-AzOperationalInsightsIntelligencePack -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -IntelligencePackName "ContosoWorkspace" -Enabled $True
```

<span data-ttu-id="fef95-109">Esse comando habilita o Pacote de Inteligência especificado.</span><span class="sxs-lookup"><span data-stu-id="fef95-109">This command enables the specified Intelligence Pack.</span></span>

## <span data-ttu-id="fef95-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fef95-110">PARAMETERS</span></span>

### <span data-ttu-id="fef95-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fef95-111">-DefaultProfile</span></span>
<span data-ttu-id="fef95-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="fef95-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fef95-113">-Habilitado</span><span class="sxs-lookup"><span data-stu-id="fef95-113">-Enabled</span></span>
```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fef95-114">-IntelligencePackName</span><span class="sxs-lookup"><span data-stu-id="fef95-114">-IntelligencePackName</span></span>
<span data-ttu-id="fef95-115">Especifica o nome do Pacote de Inteligência.</span><span class="sxs-lookup"><span data-stu-id="fef95-115">Specifies the Intelligence Pack name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fef95-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fef95-116">-ResourceGroupName</span></span>
<span data-ttu-id="fef95-117">Especifica o nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="fef95-117">Specifies the resource group name</span></span>

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

### <span data-ttu-id="fef95-118">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="fef95-118">-WorkspaceName</span></span>
<span data-ttu-id="fef95-119">Especifica o nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="fef95-119">Specifies the name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fef95-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fef95-120">CommonParameters</span></span>
<span data-ttu-id="fef95-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fef95-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fef95-122">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fef95-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fef95-123">Entradas</span><span class="sxs-lookup"><span data-stu-id="fef95-123">INPUTS</span></span>

### <span data-ttu-id="fef95-124">System.String</span><span class="sxs-lookup"><span data-stu-id="fef95-124">System.String</span></span>

### <span data-ttu-id="fef95-125">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fef95-125">System.Boolean</span></span>

## <span data-ttu-id="fef95-126">Saídas</span><span class="sxs-lookup"><span data-stu-id="fef95-126">OUTPUTS</span></span>

### <span data-ttu-id="fef95-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="fef95-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack</span></span>

## <span data-ttu-id="fef95-128">Notas</span><span class="sxs-lookup"><span data-stu-id="fef95-128">NOTES</span></span>

## <span data-ttu-id="fef95-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fef95-129">RELATED LINKS</span></span>

[<span data-ttu-id="fef95-130">Cmdlets de Insights Operacionais do Azure</span><span class="sxs-lookup"><span data-stu-id="fef95-130">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


