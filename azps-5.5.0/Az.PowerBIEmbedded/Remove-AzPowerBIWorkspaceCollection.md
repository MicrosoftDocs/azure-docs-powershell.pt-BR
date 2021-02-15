---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 2D63CC6D-AB02-4299-A922-4057D6F595D7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/remove-azpowerbiworkspacecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Remove-AzPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Remove-AzPowerBIWorkspaceCollection.md
ms.openlocfilehash: c8e6f54b5bd4deeb4ef24559298306880740c6d3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114567"
---
# <span data-ttu-id="447cb-101">Remove-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="447cb-101">Remove-AzPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="447cb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="447cb-102">SYNOPSIS</span></span>
<span data-ttu-id="447cb-103">Remove uma coleção de espaços de trabalho do Power BI.</span><span class="sxs-lookup"><span data-stu-id="447cb-103">Removes a Power BI workspace collection.</span></span>

## <span data-ttu-id="447cb-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="447cb-104">SYNTAX</span></span>

```
Remove-AzPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="447cb-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="447cb-105">DESCRIPTION</span></span>
<span data-ttu-id="447cb-106">O cmdlet **Remove-AzPowerBIWorkspaceCollection** remove um conjunto de espaços de trabalho do Power BI da sua assinatura do Azure e do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="447cb-106">The **Remove-AzPowerBIWorkspaceCollection** cmdlet removes a Power BI workspace collection from your Azure subscription and resource group.</span></span>

## <span data-ttu-id="447cb-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="447cb-107">EXAMPLES</span></span>

### <span data-ttu-id="447cb-108">Exemplo 1: Remover um conjunto de espaços de trabalho</span><span class="sxs-lookup"><span data-stu-id="447cb-108">Example 1: Remove a workspace collection</span></span>
```
PS C:\>Remove-AzPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="447cb-109">Esse comando remove o conjunto de espaços de trabalho chamado WCN11 no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="447cb-109">This command removes the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="447cb-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="447cb-110">PARAMETERS</span></span>

### <span data-ttu-id="447cb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="447cb-111">-DefaultProfile</span></span>
<span data-ttu-id="447cb-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="447cb-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="447cb-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="447cb-113">-ResourceGroupName</span></span>
<span data-ttu-id="447cb-114">Especifica o nome do grupo de recursos do qual este cmdlet remove um conjunto de espaços de trabalho.</span><span class="sxs-lookup"><span data-stu-id="447cb-114">Specifies the name of the resource group from which this cmdlet removes a workspace collection.</span></span>

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

### <span data-ttu-id="447cb-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="447cb-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="447cb-116">Especifica o nome da coleção de espaços de trabalho do Power BI que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="447cb-116">Specifies the name of the Power BI workspace collection that this cmdlet removes.</span></span>

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

### <span data-ttu-id="447cb-117">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="447cb-117">-Confirm</span></span>
<span data-ttu-id="447cb-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="447cb-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="447cb-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="447cb-119">-WhatIf</span></span>
<span data-ttu-id="447cb-120">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="447cb-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="447cb-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="447cb-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="447cb-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="447cb-122">CommonParameters</span></span>
<span data-ttu-id="447cb-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="447cb-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="447cb-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="447cb-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="447cb-125">Entradas</span><span class="sxs-lookup"><span data-stu-id="447cb-125">INPUTS</span></span>

### <span data-ttu-id="447cb-126">System.String</span><span class="sxs-lookup"><span data-stu-id="447cb-126">System.String</span></span>

## <span data-ttu-id="447cb-127">Saídas</span><span class="sxs-lookup"><span data-stu-id="447cb-127">OUTPUTS</span></span>

### <span data-ttu-id="447cb-128">System.Void</span><span class="sxs-lookup"><span data-stu-id="447cb-128">System.Void</span></span>

## <span data-ttu-id="447cb-129">Notas</span><span class="sxs-lookup"><span data-stu-id="447cb-129">NOTES</span></span>

## <span data-ttu-id="447cb-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="447cb-130">RELATED LINKS</span></span>

[<span data-ttu-id="447cb-131">Get-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="447cb-131">Get-AzPowerBIWorkspaceCollection</span></span>](./Get-AzPowerBIWorkspaceCollection.md)

[<span data-ttu-id="447cb-132">New-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="447cb-132">New-AzPowerBIWorkspaceCollection</span></span>](./New-AzPowerBIWorkspaceCollection.md)


