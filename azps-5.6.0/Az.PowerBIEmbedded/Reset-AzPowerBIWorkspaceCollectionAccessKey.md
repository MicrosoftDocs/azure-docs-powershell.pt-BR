---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 8FB2D9A0-BF7A-482D-B3A2-566FCA8C62A1
online version: https://docs.microsoft.com/powershell/module/az.powerbiembedded/reset-azpowerbiworkspacecollectionaccesskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Reset-AzPowerBIWorkspaceCollectionAccessKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Reset-AzPowerBIWorkspaceCollectionAccessKey.md
ms.openlocfilehash: 2685013ed07eef18ed1b9ac78631c37acf52b205
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885564"
---
# <span data-ttu-id="19544-101">Reset-AzPowerBIWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="19544-101">Reset-AzPowerBIWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="19544-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19544-102">SYNOPSIS</span></span>
<span data-ttu-id="19544-103">Redefine a chave de acesso especificada.</span><span class="sxs-lookup"><span data-stu-id="19544-103">Resets the specified access key.</span></span>

## <span data-ttu-id="19544-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="19544-104">SYNTAX</span></span>

```
Reset-AzPowerBIWorkspaceCollectionAccessKey [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-Key1] [-Key2] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19544-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="19544-105">DESCRIPTION</span></span>
<span data-ttu-id="19544-106">O cmdlet **Reset-AzPowerBIWorkspaceCollectionAccessKey** redefine a chave de acesso especificada em sua coleção de espaços de trabalho do Power BI.</span><span class="sxs-lookup"><span data-stu-id="19544-106">The **Reset-AzPowerBIWorkspaceCollectionAccessKey** cmdlet resets the specified access key in your Power BI workspace collection.</span></span>

## <span data-ttu-id="19544-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="19544-107">EXAMPLES</span></span>

### <span data-ttu-id="19544-108">Exemplo 1: Redefinir a chave de acesso principal</span><span class="sxs-lookup"><span data-stu-id="19544-108">Example 1: Reset the primary access key</span></span>
```
PS C:\>Reset-AzPowerBIWorkspaceCollectionAccessKey -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11" -Key1
```

<span data-ttu-id="19544-109">Este comando redefine a chave de acesso principal para a coleção de espaços de trabalho chamada WCN11 no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="19544-109">This command resets the primary access key for the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="19544-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="19544-110">PARAMETERS</span></span>

### <span data-ttu-id="19544-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19544-111">-DefaultProfile</span></span>
<span data-ttu-id="19544-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="19544-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="19544-113">-Key1</span><span class="sxs-lookup"><span data-stu-id="19544-113">-Key1</span></span>
<span data-ttu-id="19544-114">Indica que esse cmdlet redefine a chave de acesso principal.</span><span class="sxs-lookup"><span data-stu-id="19544-114">Indicates that this cmdlet resets the primary access key.</span></span>

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

### <span data-ttu-id="19544-115">-Key2</span><span class="sxs-lookup"><span data-stu-id="19544-115">-Key2</span></span>
<span data-ttu-id="19544-116">Indica que esse cmdlet redefine a chave de acesso secundária.</span><span class="sxs-lookup"><span data-stu-id="19544-116">Indicates that this cmdlet resets the secondary access key.</span></span>

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

### <span data-ttu-id="19544-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19544-117">-ResourceGroupName</span></span>
<span data-ttu-id="19544-118">Especifica o nome do grupo de recursos da coleção.</span><span class="sxs-lookup"><span data-stu-id="19544-118">Specifies the name of the resource group of the collection.</span></span>

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

### <span data-ttu-id="19544-119">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="19544-119">-WorkspaceCollectionName</span></span>
<span data-ttu-id="19544-120">Especifica o nome da coleção de espaços de trabalho do Power BI no qual esse cmdlet opera.</span><span class="sxs-lookup"><span data-stu-id="19544-120">Specifies the name of the Power BI workspace collection on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="19544-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="19544-121">-Confirm</span></span>
<span data-ttu-id="19544-122">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19544-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19544-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19544-123">-WhatIf</span></span>
<span data-ttu-id="19544-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="19544-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19544-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="19544-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19544-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19544-126">CommonParameters</span></span>
<span data-ttu-id="19544-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19544-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19544-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19544-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19544-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="19544-129">INPUTS</span></span>

### <span data-ttu-id="19544-130">System.String</span><span class="sxs-lookup"><span data-stu-id="19544-130">System.String</span></span>

## <span data-ttu-id="19544-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="19544-131">OUTPUTS</span></span>

### <span data-ttu-id="19544-132">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="19544-132">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="19544-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="19544-133">NOTES</span></span>

## <span data-ttu-id="19544-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="19544-134">RELATED LINKS</span></span>

[<span data-ttu-id="19544-135">Get-AzPowerBIWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="19544-135">Get-AzPowerBIWorkspaceCollectionAccessKey</span></span>](./Get-AzPowerBIWorkspaceCollectionAccessKey.md)


