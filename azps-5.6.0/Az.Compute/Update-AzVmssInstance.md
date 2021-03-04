---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: E8C9D68E-7C68-43D0-B348-72E9713CB99F
online version: https://docs.microsoft.com/powershell/module/az.compute/update-azvmssinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssInstance.md
ms.openlocfilehash: ed0ad08d94cbc67832b6a0dbb85882bd18692d5c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890643"
---
# <span data-ttu-id="43e59-101">Update-AzVmssInstance</span><span class="sxs-lookup"><span data-stu-id="43e59-101">Update-AzVmssInstance</span></span>

## <span data-ttu-id="43e59-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43e59-102">SYNOPSIS</span></span>
<span data-ttu-id="43e59-103">Inicia uma atualização manual da instância VMSS.</span><span class="sxs-lookup"><span data-stu-id="43e59-103">Starts a manual upgrade of the VMSS instance.</span></span>

## <span data-ttu-id="43e59-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="43e59-104">SYNTAX</span></span>

```
Update-AzVmssInstance [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43e59-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="43e59-105">DESCRIPTION</span></span>
<span data-ttu-id="43e59-106">O Update-AzVmssInstance cmdlet inicia uma atualização manual da instância do Conjunto de Escala de Máquina Virtual (VMSS) especificada.</span><span class="sxs-lookup"><span data-stu-id="43e59-106">The Update-AzVmssInstance cmdlet starts a manual upgrade of the specified Virtual Machine Scale Set (VMSS) instance.</span></span>
<span data-ttu-id="43e59-107">Isso é usado quando a política de atualização no Conjunto de Escala VMSS é definida como manual.</span><span class="sxs-lookup"><span data-stu-id="43e59-107">This is used when the upgrade policy on the VMSS Scale Set is set to manual.</span></span>

## <span data-ttu-id="43e59-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="43e59-108">EXAMPLES</span></span>

### <span data-ttu-id="43e59-109">Exemplo 1: Iniciar uma atualização da instância VMSS</span><span class="sxs-lookup"><span data-stu-id="43e59-109">Example 1: Start an upgrade of the VMSS instance</span></span>
```
PS C:\> Update-AzVmssInstance -ResourceGroupName "Group011" -VMScaleSetName "VMScaleSet001" -InstanceId "0"
```

<span data-ttu-id="43e59-110">Este comando inicia uma atualização do VMSS chamado VMScaleSet001 que tem a ID da instância de 0.</span><span class="sxs-lookup"><span data-stu-id="43e59-110">This command starts an upgrade of the VMSS named VMScaleSet001 that has the instance ID of 0.</span></span>

## <span data-ttu-id="43e59-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="43e59-111">PARAMETERS</span></span>

### <span data-ttu-id="43e59-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="43e59-112">-AsJob</span></span>
<span data-ttu-id="43e59-113">Execute o cmdlet em segundo plano e retorne um Trabalho para controlar o progresso.</span><span class="sxs-lookup"><span data-stu-id="43e59-113">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="43e59-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43e59-114">-DefaultProfile</span></span>
<span data-ttu-id="43e59-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="43e59-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="43e59-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="43e59-116">-InstanceId</span></span>
<span data-ttu-id="43e59-117">Especifica, como uma matriz de cadeia de caracteres, as IDs ou IDs da instância a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="43e59-117">Specifies, as a string array, the ID or IDs of the instance to upgrade.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43e59-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43e59-118">-ResourceGroupName</span></span>
<span data-ttu-id="43e59-119">Especifica o nome do grupo de recursos do VMSS.</span><span class="sxs-lookup"><span data-stu-id="43e59-119">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="43e59-120">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="43e59-120">-VMScaleSetName</span></span>
<span data-ttu-id="43e59-121">Especifica o nome da instância VMSS que este cmdlet atualiza.</span><span class="sxs-lookup"><span data-stu-id="43e59-121">Specifies the name of the VMSS instance that this cmdlet upgrades.</span></span>

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

### <span data-ttu-id="43e59-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="43e59-122">-Confirm</span></span>
<span data-ttu-id="43e59-123">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43e59-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43e59-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43e59-124">-WhatIf</span></span>
<span data-ttu-id="43e59-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="43e59-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43e59-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="43e59-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43e59-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43e59-127">CommonParameters</span></span>
<span data-ttu-id="43e59-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43e59-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43e59-129">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="43e59-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43e59-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="43e59-130">INPUTS</span></span>

### <span data-ttu-id="43e59-131">System.String</span><span class="sxs-lookup"><span data-stu-id="43e59-131">System.String</span></span>

### <span data-ttu-id="43e59-132">System.String[]</span><span class="sxs-lookup"><span data-stu-id="43e59-132">System.String[]</span></span>

## <span data-ttu-id="43e59-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="43e59-133">OUTPUTS</span></span>

### <span data-ttu-id="43e59-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="43e59-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="43e59-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="43e59-135">NOTES</span></span>

## <span data-ttu-id="43e59-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="43e59-136">RELATED LINKS</span></span>

[<span data-ttu-id="43e59-137">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="43e59-137">Update-AzVmss</span></span>](./Update-AzVmss.md)


