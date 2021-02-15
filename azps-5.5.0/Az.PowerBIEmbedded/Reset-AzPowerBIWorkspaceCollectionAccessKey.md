---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 8FB2D9A0-BF7A-482D-B3A2-566FCA8C62A1
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/reset-azpowerbiworkspacecollectionaccesskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Reset-AzPowerBIWorkspaceCollectionAccessKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Reset-AzPowerBIWorkspaceCollectionAccessKey.md
ms.openlocfilehash: d9e30c81eb0e2422b91be79bcfc7c732291c30cb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114566"
---
# <span data-ttu-id="b4f7d-101">Reset-AzPowerBIWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="b4f7d-101">Reset-AzPowerBIWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="b4f7d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b4f7d-102">SYNOPSIS</span></span>
<span data-ttu-id="b4f7d-103">Redefine a tecla de acesso especificada.</span><span class="sxs-lookup"><span data-stu-id="b4f7d-103">Resets the specified access key.</span></span>

## <span data-ttu-id="b4f7d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b4f7d-104">SYNTAX</span></span>

```
Reset-AzPowerBIWorkspaceCollectionAccessKey [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-Key1] [-Key2] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4f7d-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="b4f7d-105">DESCRIPTION</span></span>
<span data-ttu-id="b4f7d-106">O cmdlet **Reset-AzPowerBIWorkspaceCollectionAccessKey** redefine a chave de acesso especificada no seu conjunto de espaços de trabalho do Power BI.</span><span class="sxs-lookup"><span data-stu-id="b4f7d-106">The **Reset-AzPowerBIWorkspaceCollectionAccessKey** cmdlet resets the specified access key in your Power BI workspace collection.</span></span>

## <span data-ttu-id="b4f7d-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b4f7d-107">EXAMPLES</span></span>

### <span data-ttu-id="b4f7d-108">Exemplo 1: Redefinir a chave de acesso principal</span><span class="sxs-lookup"><span data-stu-id="b4f7d-108">Example 1: Reset the primary access key</span></span>
```
PS C:\>Reset-AzPowerBIWorkspaceCollectionAccessKey -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11" -Key1
```

<span data-ttu-id="b4f7d-109">Esse comando redefine a chave de acesso principal do conjunto de espaços de trabalho chamado WCN11 no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="b4f7d-109">This command resets the primary access key for the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="b4f7d-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b4f7d-110">PARAMETERS</span></span>

### <span data-ttu-id="b4f7d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4f7d-111">-DefaultProfile</span></span>
<span data-ttu-id="b4f7d-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="b4f7d-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b4f7d-113">-Tecla1</span><span class="sxs-lookup"><span data-stu-id="b4f7d-113">-Key1</span></span>
<span data-ttu-id="b4f7d-114">Indica que esse cmdlet redefine a chave de acesso principal.</span><span class="sxs-lookup"><span data-stu-id="b4f7d-114">Indicates that this cmdlet resets the primary access key.</span></span>

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

### <span data-ttu-id="b4f7d-115">-Tecla2</span><span class="sxs-lookup"><span data-stu-id="b4f7d-115">-Key2</span></span>
<span data-ttu-id="b4f7d-116">Indica que esse cmdlet redefine a tecla de acesso secundária.</span><span class="sxs-lookup"><span data-stu-id="b4f7d-116">Indicates that this cmdlet resets the secondary access key.</span></span>

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

### <span data-ttu-id="b4f7d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4f7d-117">-ResourceGroupName</span></span>
<span data-ttu-id="b4f7d-118">Especifica o nome do grupo de recursos da coleção.</span><span class="sxs-lookup"><span data-stu-id="b4f7d-118">Specifies the name of the resource group of the collection.</span></span>

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

### <span data-ttu-id="b4f7d-119">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="b4f7d-119">-WorkspaceCollectionName</span></span>
<span data-ttu-id="b4f7d-120">Especifica o nome do conjunto de espaços de trabalho do Power BI no qual este cmdlet opera.</span><span class="sxs-lookup"><span data-stu-id="b4f7d-120">Specifies the name of the Power BI workspace collection on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="b4f7d-121">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="b4f7d-121">-Confirm</span></span>
<span data-ttu-id="b4f7d-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4f7d-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4f7d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4f7d-123">-WhatIf</span></span>
<span data-ttu-id="b4f7d-124">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="b4f7d-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4f7d-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b4f7d-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4f7d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4f7d-126">CommonParameters</span></span>
<span data-ttu-id="b4f7d-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4f7d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4f7d-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4f7d-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4f7d-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="b4f7d-129">INPUTS</span></span>

### <span data-ttu-id="b4f7d-130">System.String</span><span class="sxs-lookup"><span data-stu-id="b4f7d-130">System.String</span></span>

## <span data-ttu-id="b4f7d-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="b4f7d-131">OUTPUTS</span></span>

### <span data-ttu-id="b4f7d-132">Microsoft.Azure.Commands.Management.PowerBIEmbekey.Models.PSWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="b4f7d-132">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="b4f7d-133">Notas</span><span class="sxs-lookup"><span data-stu-id="b4f7d-133">NOTES</span></span>

## <span data-ttu-id="b4f7d-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b4f7d-134">RELATED LINKS</span></span>

[<span data-ttu-id="b4f7d-135">Get-AzPowerBIWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="b4f7d-135">Get-AzPowerBIWorkspaceCollectionAccessKey</span></span>](./Get-AzPowerBIWorkspaceCollectionAccessKey.md)


