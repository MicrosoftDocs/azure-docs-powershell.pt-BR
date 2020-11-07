---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: E8C9D68E-7C68-43D0-B348-72E9713CB99F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermvmssinstance
schema: 2.0.0
ms.openlocfilehash: 07b068587848bc8af92fc49b039155c0a2c4fdd8
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786123"
---
# <span data-ttu-id="e8825-101">Update-AzureRmVmssInstance</span><span class="sxs-lookup"><span data-stu-id="e8825-101">Update-AzureRmVmssInstance</span></span>

## <span data-ttu-id="e8825-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e8825-102">SYNOPSIS</span></span>
<span data-ttu-id="e8825-103">Inicia uma atualização manual da instância VMSS.</span><span class="sxs-lookup"><span data-stu-id="e8825-103">Starts a manual upgrade of the VMSS instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e8825-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e8825-104">SYNTAX</span></span>

```
Update-AzureRmVmssInstance [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8825-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e8825-105">DESCRIPTION</span></span>
<span data-ttu-id="e8825-106">O cmdlet Update-AzureRmVmssInstance inicia uma atualização manual da instância especificada do conjunto de dimensionamento de máquina virtual (VMSS).</span><span class="sxs-lookup"><span data-stu-id="e8825-106">The Update-AzureRmVmssInstance cmdlet starts a manual upgrade of the specified Virtual Machine Scale Set (VMSS) instance.</span></span>
<span data-ttu-id="e8825-107">Isso é usado quando a política de atualização do conjunto de escala VMSS é definida como manual.</span><span class="sxs-lookup"><span data-stu-id="e8825-107">This is used when the upgrade policy on the VMSS Scale Set is set to manual.</span></span>

## <span data-ttu-id="e8825-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e8825-108">EXAMPLES</span></span>

### <span data-ttu-id="e8825-109">Exemplo 1: iniciar uma atualização da instância VMSS</span><span class="sxs-lookup"><span data-stu-id="e8825-109">Example 1: Start an upgrade of the VMSS instance</span></span>
```
PS C:\> Update-AzureRmVmssInstance -ResourceGroupName "Group011" -VMScaleSetName "VMScaleSet001" -InstanceId "0"
```

<span data-ttu-id="e8825-110">Esse comando inicia uma atualização do VMSS chamado VMScaleSet001 que tem a ID de instância 0.</span><span class="sxs-lookup"><span data-stu-id="e8825-110">This command starts an upgrade of the VMSS named VMScaleSet001 that has the instance ID of 0.</span></span>

## <span data-ttu-id="e8825-111">OS</span><span class="sxs-lookup"><span data-stu-id="e8825-111">PARAMETERS</span></span>

### <span data-ttu-id="e8825-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e8825-112">-AsJob</span></span>
<span data-ttu-id="e8825-113">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="e8825-113">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8825-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8825-114">-DefaultProfile</span></span>
<span data-ttu-id="e8825-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e8825-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8825-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="e8825-116">-InstanceId</span></span>
<span data-ttu-id="e8825-117">Especifica, como uma matriz de cadeia de caracteres, a ID ou IDs da instância a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="e8825-117">Specifies, as a string array, the ID or IDs of the instance to upgrade.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8825-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8825-118">-ResourceGroupName</span></span>
<span data-ttu-id="e8825-119">Especifica o nome do grupo de recursos do VMSS.</span><span class="sxs-lookup"><span data-stu-id="e8825-119">Specifies the name of the resource group of the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8825-120">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="e8825-120">-VMScaleSetName</span></span>
<span data-ttu-id="e8825-121">Especifica o nome da instância VMSS que este cmdlet atualiza.</span><span class="sxs-lookup"><span data-stu-id="e8825-121">Specifies the name of the VMSS instance that this cmdlet upgrades.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8825-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e8825-122">-Confirm</span></span>
<span data-ttu-id="e8825-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8825-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8825-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8825-124">-WhatIf</span></span>
<span data-ttu-id="e8825-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e8825-125">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="e8825-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e8825-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8825-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8825-127">CommonParameters</span></span>
<span data-ttu-id="e8825-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8825-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8825-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8825-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8825-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e8825-130">INPUTS</span></span>

### <span data-ttu-id="e8825-131">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="e8825-131">None</span></span>
<span data-ttu-id="e8825-132">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="e8825-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e8825-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e8825-133">OUTPUTS</span></span>

###  
<span data-ttu-id="e8825-134">Esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="e8825-134">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="e8825-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e8825-135">NOTES</span></span>

## <span data-ttu-id="e8825-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e8825-136">RELATED LINKS</span></span>

[<span data-ttu-id="e8825-137">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e8825-137">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


