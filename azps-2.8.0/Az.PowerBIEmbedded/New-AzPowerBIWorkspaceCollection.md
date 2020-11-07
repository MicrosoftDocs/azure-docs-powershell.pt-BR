---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 9F9E4273-6747-4963-AF1F-C0AEB46770A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/new-azpowerbiworkspacecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/New-AzPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/New-AzPowerBIWorkspaceCollection.md
ms.openlocfilehash: c16632f621af0dfe3f6b6a1b53148eef2c480e8a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772804"
---
# <span data-ttu-id="78a75-101">New-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="78a75-101">New-AzPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="78a75-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="78a75-102">SYNOPSIS</span></span>
<span data-ttu-id="78a75-103">Cria um conjunto de espaço de trabalho do Power BI.</span><span class="sxs-lookup"><span data-stu-id="78a75-103">Creates a Power BI workspace collection.</span></span>

## <span data-ttu-id="78a75-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="78a75-104">SYNTAX</span></span>

```
New-AzPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78a75-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="78a75-105">DESCRIPTION</span></span>
<span data-ttu-id="78a75-106">O cmdlet **New-AzPowerBIWorkspaceCollection** cria um conjunto do espaço de trabalho do Power bi para a sua assinatura do Azure no grupo de recursos e local especificados.</span><span class="sxs-lookup"><span data-stu-id="78a75-106">The **New-AzPowerBIWorkspaceCollection** cmdlet creates a Power BI workspace collection for your Azure subscription in the specified resource group and location.</span></span>

## <span data-ttu-id="78a75-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="78a75-107">EXAMPLES</span></span>

### <span data-ttu-id="78a75-108">Exemplo 1: criar uma coleção de espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="78a75-108">Example 1: Create a workspace collection</span></span>
```
PS C:\>New-AzPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11" -Location "Japan West"
```

<span data-ttu-id="78a75-109">Esse comando cria um conjunto de espaços de trabalho denominado WCN11 no grupo de recursos especificado no local especificado.</span><span class="sxs-lookup"><span data-stu-id="78a75-109">This command creates a workspace collection named WCN11 in the specified resource group in the specified location.</span></span>

## <span data-ttu-id="78a75-110">OS</span><span class="sxs-lookup"><span data-stu-id="78a75-110">PARAMETERS</span></span>

### <span data-ttu-id="78a75-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78a75-111">-DefaultProfile</span></span>
<span data-ttu-id="78a75-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="78a75-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="78a75-113">-Local</span><span class="sxs-lookup"><span data-stu-id="78a75-113">-Location</span></span>
<span data-ttu-id="78a75-114">Especifica o local do Azure no qual esse cmdlet cria uma coleção de espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="78a75-114">Specifies the Azure location in which this cmdlet creates a workspace collection.</span></span>

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

### <span data-ttu-id="78a75-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78a75-115">-ResourceGroupName</span></span>
<span data-ttu-id="78a75-116">Especifica o nome do grupo de recursos em que esse cmdlet cria uma coleção de espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="78a75-116">Specifies the name of the resource group in which this cmdlet creates a workspace collection.</span></span>

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

### <span data-ttu-id="78a75-117">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="78a75-117">-WorkspaceCollectionName</span></span>
<span data-ttu-id="78a75-118">Especifica um nome para o conjunto do espaço de trabalho do Power BI.</span><span class="sxs-lookup"><span data-stu-id="78a75-118">Specifies a name for the Power BI workspace collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78a75-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="78a75-119">-Confirm</span></span>
<span data-ttu-id="78a75-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78a75-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78a75-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78a75-121">-WhatIf</span></span>
<span data-ttu-id="78a75-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="78a75-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78a75-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="78a75-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78a75-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78a75-124">CommonParameters</span></span>
<span data-ttu-id="78a75-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78a75-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78a75-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78a75-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78a75-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="78a75-127">INPUTS</span></span>

### <span data-ttu-id="78a75-128">System. String</span><span class="sxs-lookup"><span data-stu-id="78a75-128">System.String</span></span>

## <span data-ttu-id="78a75-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="78a75-129">OUTPUTS</span></span>

### <span data-ttu-id="78a75-130">Microsoft. Azure. Commands. Management. PowerBIEmbedded. Models. PSWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="78a75-130">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollection</span></span>

## <span data-ttu-id="78a75-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="78a75-131">NOTES</span></span>

## <span data-ttu-id="78a75-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="78a75-132">RELATED LINKS</span></span>

[<span data-ttu-id="78a75-133">Get-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="78a75-133">Get-AzPowerBIWorkspaceCollection</span></span>](./Get-AzPowerBIWorkspaceCollection.md)

[<span data-ttu-id="78a75-134">Remove-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="78a75-134">Remove-AzPowerBIWorkspaceCollection</span></span>](./Remove-AzPowerBIWorkspaceCollection.md)


