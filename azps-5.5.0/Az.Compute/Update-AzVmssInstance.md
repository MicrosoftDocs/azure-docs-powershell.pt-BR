---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: E8C9D68E-7C68-43D0-B348-72E9713CB99F
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmssinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssInstance.md
ms.openlocfilehash: f7adb9ef086b233d44f2e5d9c6eb132669b102e5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115458"
---
# <span data-ttu-id="6b347-101">Update-AzVmssInstance</span><span class="sxs-lookup"><span data-stu-id="6b347-101">Update-AzVmssInstance</span></span>

## <span data-ttu-id="6b347-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6b347-102">SYNOPSIS</span></span>
<span data-ttu-id="6b347-103">Inicia uma atualização manual da instância VMSS.</span><span class="sxs-lookup"><span data-stu-id="6b347-103">Starts a manual upgrade of the VMSS instance.</span></span>

## <span data-ttu-id="6b347-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6b347-104">SYNTAX</span></span>

```
Update-AzVmssInstance [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b347-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="6b347-105">DESCRIPTION</span></span>
<span data-ttu-id="6b347-106">O Update-AzVmssInstance cmdlet inicia uma atualização manual da instância do VMSS (Conjunto de Escala de Máquina Virtual) especificada.</span><span class="sxs-lookup"><span data-stu-id="6b347-106">The Update-AzVmssInstance cmdlet starts a manual upgrade of the specified Virtual Machine Scale Set (VMSS) instance.</span></span>
<span data-ttu-id="6b347-107">Isso é usado quando a política de atualização no Conjunto de Escala do VMSS é definida como manual.</span><span class="sxs-lookup"><span data-stu-id="6b347-107">This is used when the upgrade policy on the VMSS Scale Set is set to manual.</span></span>

## <span data-ttu-id="6b347-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6b347-108">EXAMPLES</span></span>

### <span data-ttu-id="6b347-109">Exemplo 1: Iniciar uma atualização da instância VMSS</span><span class="sxs-lookup"><span data-stu-id="6b347-109">Example 1: Start an upgrade of the VMSS instance</span></span>
```
PS C:\> Update-AzVmssInstance -ResourceGroupName "Group011" -VMScaleSetName "VMScaleSet001" -InstanceId "0"
```

<span data-ttu-id="6b347-110">Esse comando inicia uma atualização do VMSS chamado VMScaleSet001 que tem a ID de instância de 0.</span><span class="sxs-lookup"><span data-stu-id="6b347-110">This command starts an upgrade of the VMSS named VMScaleSet001 that has the instance ID of 0.</span></span>

## <span data-ttu-id="6b347-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6b347-111">PARAMETERS</span></span>

### <span data-ttu-id="6b347-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6b347-112">-AsJob</span></span>
<span data-ttu-id="6b347-113">Execute o cmdlet em segundo plano e retorne um Trabalho para controlar o andamento.</span><span class="sxs-lookup"><span data-stu-id="6b347-113">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="6b347-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b347-114">-DefaultProfile</span></span>
<span data-ttu-id="6b347-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="6b347-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b347-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="6b347-116">-InstanceId</span></span>
<span data-ttu-id="6b347-117">Especifica, como uma matriz de cadeia de caracteres, as IDs ou IDs da instância para atualizar.</span><span class="sxs-lookup"><span data-stu-id="6b347-117">Specifies, as a string array, the ID or IDs of the instance to upgrade.</span></span>

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

### <span data-ttu-id="6b347-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b347-118">-ResourceGroupName</span></span>
<span data-ttu-id="6b347-119">Especifica o nome do grupo de recursos do VMSS.</span><span class="sxs-lookup"><span data-stu-id="6b347-119">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="6b347-120">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="6b347-120">-VMScaleSetName</span></span>
<span data-ttu-id="6b347-121">Especifica o nome da instância VMSS que este cmdlet atualiza.</span><span class="sxs-lookup"><span data-stu-id="6b347-121">Specifies the name of the VMSS instance that this cmdlet upgrades.</span></span>

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

### <span data-ttu-id="6b347-122">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="6b347-122">-Confirm</span></span>
<span data-ttu-id="6b347-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b347-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b347-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b347-124">-WhatIf</span></span>
<span data-ttu-id="6b347-125">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="6b347-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b347-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6b347-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b347-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b347-127">CommonParameters</span></span>
<span data-ttu-id="6b347-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b347-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b347-129">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6b347-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b347-130">Entradas</span><span class="sxs-lookup"><span data-stu-id="6b347-130">INPUTS</span></span>

### <span data-ttu-id="6b347-131">System.String</span><span class="sxs-lookup"><span data-stu-id="6b347-131">System.String</span></span>

### <span data-ttu-id="6b347-132">System.String[]</span><span class="sxs-lookup"><span data-stu-id="6b347-132">System.String[]</span></span>

## <span data-ttu-id="6b347-133">Saídas</span><span class="sxs-lookup"><span data-stu-id="6b347-133">OUTPUTS</span></span>

### <span data-ttu-id="6b347-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="6b347-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="6b347-135">Notas</span><span class="sxs-lookup"><span data-stu-id="6b347-135">NOTES</span></span>

## <span data-ttu-id="6b347-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6b347-136">RELATED LINKS</span></span>

[<span data-ttu-id="6b347-137">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6b347-137">Update-AzVmss</span></span>](./Update-AzVmss.md)


