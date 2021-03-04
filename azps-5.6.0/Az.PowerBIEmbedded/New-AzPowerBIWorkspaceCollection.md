---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 9F9E4273-6747-4963-AF1F-C0AEB46770A4
online version: https://docs.microsoft.com/powershell/module/az.powerbiembedded/new-azpowerbiworkspacecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/New-AzPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/New-AzPowerBIWorkspaceCollection.md
ms.openlocfilehash: 69f90f84d7e142ea3471c7e6871baac145f1b9c0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888202"
---
# <span data-ttu-id="f156c-101">New-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="f156c-101">New-AzPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="f156c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f156c-102">SYNOPSIS</span></span>
<span data-ttu-id="f156c-103">Cria uma coleção de espaços de trabalho do Power BI.</span><span class="sxs-lookup"><span data-stu-id="f156c-103">Creates a Power BI workspace collection.</span></span>

## <span data-ttu-id="f156c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f156c-104">SYNTAX</span></span>

```
New-AzPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f156c-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f156c-105">DESCRIPTION</span></span>
<span data-ttu-id="f156c-106">O cmdlet **New-AzPowerBIWorkspaceCollection** cria uma coleção de espaços de trabalho do Power BI para sua assinatura do Azure no grupo de recursos especificado e no local.</span><span class="sxs-lookup"><span data-stu-id="f156c-106">The **New-AzPowerBIWorkspaceCollection** cmdlet creates a Power BI workspace collection for your Azure subscription in the specified resource group and location.</span></span>

## <span data-ttu-id="f156c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f156c-107">EXAMPLES</span></span>

### <span data-ttu-id="f156c-108">Exemplo 1: Criar uma coleção de espaços de trabalho</span><span class="sxs-lookup"><span data-stu-id="f156c-108">Example 1: Create a workspace collection</span></span>
```
PS C:\>New-AzPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11" -Location "Japan West"
```

<span data-ttu-id="f156c-109">Este comando cria uma coleção de espaços de trabalho chamada WCN11 no grupo de recursos especificado no local especificado.</span><span class="sxs-lookup"><span data-stu-id="f156c-109">This command creates a workspace collection named WCN11 in the specified resource group in the specified location.</span></span>

## <span data-ttu-id="f156c-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f156c-110">PARAMETERS</span></span>

### <span data-ttu-id="f156c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f156c-111">-DefaultProfile</span></span>
<span data-ttu-id="f156c-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="f156c-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f156c-113">-Location</span><span class="sxs-lookup"><span data-stu-id="f156c-113">-Location</span></span>
<span data-ttu-id="f156c-114">Especifica o local do Azure no qual este cmdlet cria uma coleção de espaços de trabalho.</span><span class="sxs-lookup"><span data-stu-id="f156c-114">Specifies the Azure location in which this cmdlet creates a workspace collection.</span></span>

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

### <span data-ttu-id="f156c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f156c-115">-ResourceGroupName</span></span>
<span data-ttu-id="f156c-116">Especifica o nome do grupo de recursos no qual esse cmdlet cria uma coleção de espaços de trabalho.</span><span class="sxs-lookup"><span data-stu-id="f156c-116">Specifies the name of the resource group in which this cmdlet creates a workspace collection.</span></span>

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

### <span data-ttu-id="f156c-117">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="f156c-117">-WorkspaceCollectionName</span></span>
<span data-ttu-id="f156c-118">Especifica um nome para a coleção de espaços de trabalho do Power BI.</span><span class="sxs-lookup"><span data-stu-id="f156c-118">Specifies a name for the Power BI workspace collection.</span></span>

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

### <span data-ttu-id="f156c-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f156c-119">-Confirm</span></span>
<span data-ttu-id="f156c-120">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f156c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f156c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f156c-121">-WhatIf</span></span>
<span data-ttu-id="f156c-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f156c-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f156c-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f156c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f156c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f156c-124">CommonParameters</span></span>
<span data-ttu-id="f156c-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f156c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f156c-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f156c-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f156c-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f156c-127">INPUTS</span></span>

### <span data-ttu-id="f156c-128">System.String</span><span class="sxs-lookup"><span data-stu-id="f156c-128">System.String</span></span>

## <span data-ttu-id="f156c-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f156c-129">OUTPUTS</span></span>

### <span data-ttu-id="f156c-130">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="f156c-130">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollection</span></span>

## <span data-ttu-id="f156c-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="f156c-131">NOTES</span></span>

## <span data-ttu-id="f156c-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f156c-132">RELATED LINKS</span></span>

[<span data-ttu-id="f156c-133">Get-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="f156c-133">Get-AzPowerBIWorkspaceCollection</span></span>](./Get-AzPowerBIWorkspaceCollection.md)

[<span data-ttu-id="f156c-134">Remove-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="f156c-134">Remove-AzPowerBIWorkspaceCollection</span></span>](./Remove-AzPowerBIWorkspaceCollection.md)


