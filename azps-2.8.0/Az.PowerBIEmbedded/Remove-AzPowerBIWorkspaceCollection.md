---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 2D63CC6D-AB02-4299-A922-4057D6F595D7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/remove-azpowerbiworkspacecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Remove-AzPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Remove-AzPowerBIWorkspaceCollection.md
ms.openlocfilehash: 058a914540cd03bcf523f0300e18299c3cf084ac
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772802"
---
# <span data-ttu-id="151a0-101">Remove-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="151a0-101">Remove-AzPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="151a0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="151a0-102">SYNOPSIS</span></span>
<span data-ttu-id="151a0-103">Remove um conjunto do espaço de trabalho do Power BI.</span><span class="sxs-lookup"><span data-stu-id="151a0-103">Removes a Power BI workspace collection.</span></span>

## <span data-ttu-id="151a0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="151a0-104">SYNTAX</span></span>

```
Remove-AzPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="151a0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="151a0-105">DESCRIPTION</span></span>
<span data-ttu-id="151a0-106">O cmdlet **Remove-AzPowerBIWorkspaceCollection** remove uma coleção de espaço de trabalho do Power bi de sua assinatura do Azure e do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="151a0-106">The **Remove-AzPowerBIWorkspaceCollection** cmdlet removes a Power BI workspace collection from your Azure subscription and resource group.</span></span>

## <span data-ttu-id="151a0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="151a0-107">EXAMPLES</span></span>

### <span data-ttu-id="151a0-108">Exemplo 1: remover uma coleção de espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="151a0-108">Example 1: Remove a workspace collection</span></span>
```
PS C:\>Remove-AzPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="151a0-109">Esse comando Remove a coleção do espaço de trabalho chamado WCN11 no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="151a0-109">This command removes the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="151a0-110">OS</span><span class="sxs-lookup"><span data-stu-id="151a0-110">PARAMETERS</span></span>

### <span data-ttu-id="151a0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="151a0-111">-DefaultProfile</span></span>
<span data-ttu-id="151a0-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="151a0-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="151a0-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="151a0-113">-ResourceGroupName</span></span>
<span data-ttu-id="151a0-114">Especifica o nome do grupo de recursos do qual esse cmdlet Remove uma coleção de espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="151a0-114">Specifies the name of the resource group from which this cmdlet removes a workspace collection.</span></span>

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

### <span data-ttu-id="151a0-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="151a0-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="151a0-116">Especifica o nome da coleção do espaço de trabalho do Power BI que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="151a0-116">Specifies the name of the Power BI workspace collection that this cmdlet removes.</span></span>

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

### <span data-ttu-id="151a0-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="151a0-117">-Confirm</span></span>
<span data-ttu-id="151a0-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="151a0-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="151a0-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="151a0-119">-WhatIf</span></span>
<span data-ttu-id="151a0-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="151a0-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="151a0-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="151a0-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="151a0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="151a0-122">CommonParameters</span></span>
<span data-ttu-id="151a0-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="151a0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="151a0-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="151a0-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="151a0-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="151a0-125">INPUTS</span></span>

### <span data-ttu-id="151a0-126">System. String</span><span class="sxs-lookup"><span data-stu-id="151a0-126">System.String</span></span>

## <span data-ttu-id="151a0-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="151a0-127">OUTPUTS</span></span>

### <span data-ttu-id="151a0-128">System. void</span><span class="sxs-lookup"><span data-stu-id="151a0-128">System.Void</span></span>

## <span data-ttu-id="151a0-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="151a0-129">NOTES</span></span>

## <span data-ttu-id="151a0-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="151a0-130">RELATED LINKS</span></span>

[<span data-ttu-id="151a0-131">Get-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="151a0-131">Get-AzPowerBIWorkspaceCollection</span></span>](./Get-AzPowerBIWorkspaceCollection.md)

[<span data-ttu-id="151a0-132">New-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="151a0-132">New-AzPowerBIWorkspaceCollection</span></span>](./New-AzPowerBIWorkspaceCollection.md)

