---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 9F9E4273-6747-4963-AF1F-C0AEB46770A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/new-azpowerbiworkspacecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/New-AzPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/New-AzPowerBIWorkspaceCollection.md
ms.openlocfilehash: 557b1b7c5c2a91ec5e77729e70d2aa58f696d212
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117252"
---
# <span data-ttu-id="a91d2-101">New-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="a91d2-101">New-AzPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="a91d2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a91d2-102">SYNOPSIS</span></span>
<span data-ttu-id="a91d2-103">Cria uma coleção de espaços de trabalho do Power BI.</span><span class="sxs-lookup"><span data-stu-id="a91d2-103">Creates a Power BI workspace collection.</span></span>

## <span data-ttu-id="a91d2-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a91d2-104">SYNTAX</span></span>

```
New-AzPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a91d2-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="a91d2-105">DESCRIPTION</span></span>
<span data-ttu-id="a91d2-106">O cmdlet **New-AzPowerBIWorkspaceCollection** cria um conjunto de espaços de trabalho do Power BI para sua assinatura do Azure no grupo de recursos e no local especificados.</span><span class="sxs-lookup"><span data-stu-id="a91d2-106">The **New-AzPowerBIWorkspaceCollection** cmdlet creates a Power BI workspace collection for your Azure subscription in the specified resource group and location.</span></span>

## <span data-ttu-id="a91d2-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a91d2-107">EXAMPLES</span></span>

### <span data-ttu-id="a91d2-108">Exemplo 1: Criar um conjunto de espaços de trabalho</span><span class="sxs-lookup"><span data-stu-id="a91d2-108">Example 1: Create a workspace collection</span></span>
```
PS C:\>New-AzPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11" -Location "Japan West"
```

<span data-ttu-id="a91d2-109">Esse comando cria um conjunto de espaços de trabalho chamado WCN11 no grupo de recursos especificado no local especificado.</span><span class="sxs-lookup"><span data-stu-id="a91d2-109">This command creates a workspace collection named WCN11 in the specified resource group in the specified location.</span></span>

## <span data-ttu-id="a91d2-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a91d2-110">PARAMETERS</span></span>

### <span data-ttu-id="a91d2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a91d2-111">-DefaultProfile</span></span>
<span data-ttu-id="a91d2-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="a91d2-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a91d2-113">-Local</span><span class="sxs-lookup"><span data-stu-id="a91d2-113">-Location</span></span>
<span data-ttu-id="a91d2-114">Especifica o local do Azure no qual este cmdlet cria um conjunto de espaços de trabalho.</span><span class="sxs-lookup"><span data-stu-id="a91d2-114">Specifies the Azure location in which this cmdlet creates a workspace collection.</span></span>

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

### <span data-ttu-id="a91d2-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a91d2-115">-ResourceGroupName</span></span>
<span data-ttu-id="a91d2-116">Especifica o nome do grupo de recursos no qual este cmdlet cria um conjunto de espaços de trabalho.</span><span class="sxs-lookup"><span data-stu-id="a91d2-116">Specifies the name of the resource group in which this cmdlet creates a workspace collection.</span></span>

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

### <span data-ttu-id="a91d2-117">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="a91d2-117">-WorkspaceCollectionName</span></span>
<span data-ttu-id="a91d2-118">Especifica um nome para a coleção de espaços de trabalho do Power BI.</span><span class="sxs-lookup"><span data-stu-id="a91d2-118">Specifies a name for the Power BI workspace collection.</span></span>

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

### <span data-ttu-id="a91d2-119">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="a91d2-119">-Confirm</span></span>
<span data-ttu-id="a91d2-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a91d2-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a91d2-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a91d2-121">-WhatIf</span></span>
<span data-ttu-id="a91d2-122">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="a91d2-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a91d2-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a91d2-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a91d2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a91d2-124">CommonParameters</span></span>
<span data-ttu-id="a91d2-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a91d2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a91d2-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a91d2-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a91d2-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="a91d2-127">INPUTS</span></span>

### <span data-ttu-id="a91d2-128">System.String</span><span class="sxs-lookup"><span data-stu-id="a91d2-128">System.String</span></span>

## <span data-ttu-id="a91d2-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="a91d2-129">OUTPUTS</span></span>

### <span data-ttu-id="a91d2-130">Microsoft.Azure.Commands.Management.PowerBIEmbeed.Models.PSWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="a91d2-130">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollection</span></span>

## <span data-ttu-id="a91d2-131">Notas</span><span class="sxs-lookup"><span data-stu-id="a91d2-131">NOTES</span></span>

## <span data-ttu-id="a91d2-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a91d2-132">RELATED LINKS</span></span>

[<span data-ttu-id="a91d2-133">Get-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="a91d2-133">Get-AzPowerBIWorkspaceCollection</span></span>](./Get-AzPowerBIWorkspaceCollection.md)

[<span data-ttu-id="a91d2-134">Remove-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="a91d2-134">Remove-AzPowerBIWorkspaceCollection</span></span>](./Remove-AzPowerBIWorkspaceCollection.md)


