---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: E8C9D68E-7C68-43D0-B348-72E9713CB99F
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmssinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzVmssInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzVmssInstance.md
ms.openlocfilehash: d8fb3b740a85b4cb258fcfa08bf9f4e06032fcb9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775932"
---
# <span data-ttu-id="072ec-101">Update-AzVmssInstance</span><span class="sxs-lookup"><span data-stu-id="072ec-101">Update-AzVmssInstance</span></span>

## <span data-ttu-id="072ec-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="072ec-102">SYNOPSIS</span></span>
<span data-ttu-id="072ec-103">Inicia uma atualização manual da instância VMSS.</span><span class="sxs-lookup"><span data-stu-id="072ec-103">Starts a manual upgrade of the VMSS instance.</span></span>

## <span data-ttu-id="072ec-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="072ec-104">SYNTAX</span></span>

```
Update-AzVmssInstance [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="072ec-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="072ec-105">DESCRIPTION</span></span>
<span data-ttu-id="072ec-106">O cmdlet Update-AzVmssInstance inicia uma atualização manual da instância especificada do conjunto de dimensionamento de máquina virtual (VMSS).</span><span class="sxs-lookup"><span data-stu-id="072ec-106">The Update-AzVmssInstance cmdlet starts a manual upgrade of the specified Virtual Machine Scale Set (VMSS) instance.</span></span>
<span data-ttu-id="072ec-107">Isso é usado quando a política de atualização do conjunto de escala VMSS é definida como manual.</span><span class="sxs-lookup"><span data-stu-id="072ec-107">This is used when the upgrade policy on the VMSS Scale Set is set to manual.</span></span>

## <span data-ttu-id="072ec-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="072ec-108">EXAMPLES</span></span>

### <span data-ttu-id="072ec-109">Exemplo 1: iniciar uma atualização da instância VMSS</span><span class="sxs-lookup"><span data-stu-id="072ec-109">Example 1: Start an upgrade of the VMSS instance</span></span>
```
PS C:\> Update-AzVmssInstance -ResourceGroupName "Group011" -VMScaleSetName "VMScaleSet001" -InstanceId "0"
```

<span data-ttu-id="072ec-110">Esse comando inicia uma atualização do VMSS chamado VMScaleSet001 que tem a ID de instância 0.</span><span class="sxs-lookup"><span data-stu-id="072ec-110">This command starts an upgrade of the VMSS named VMScaleSet001 that has the instance ID of 0.</span></span>

## <span data-ttu-id="072ec-111">OS</span><span class="sxs-lookup"><span data-stu-id="072ec-111">PARAMETERS</span></span>

### <span data-ttu-id="072ec-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="072ec-112">-AsJob</span></span>
<span data-ttu-id="072ec-113">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="072ec-113">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="072ec-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="072ec-114">-DefaultProfile</span></span>
<span data-ttu-id="072ec-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="072ec-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="072ec-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="072ec-116">-InstanceId</span></span>
<span data-ttu-id="072ec-117">Especifica, como uma matriz de cadeia de caracteres, a ID ou IDs da instância a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="072ec-117">Specifies, as a string array, the ID or IDs of the instance to upgrade.</span></span>

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

### <span data-ttu-id="072ec-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="072ec-118">-ResourceGroupName</span></span>
<span data-ttu-id="072ec-119">Especifica o nome do grupo de recursos do VMSS.</span><span class="sxs-lookup"><span data-stu-id="072ec-119">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="072ec-120">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="072ec-120">-VMScaleSetName</span></span>
<span data-ttu-id="072ec-121">Especifica o nome da instância VMSS que este cmdlet atualiza.</span><span class="sxs-lookup"><span data-stu-id="072ec-121">Specifies the name of the VMSS instance that this cmdlet upgrades.</span></span>

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

### <span data-ttu-id="072ec-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="072ec-122">-Confirm</span></span>
<span data-ttu-id="072ec-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="072ec-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="072ec-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="072ec-124">-WhatIf</span></span>
<span data-ttu-id="072ec-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="072ec-125">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="072ec-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="072ec-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="072ec-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="072ec-127">CommonParameters</span></span>
<span data-ttu-id="072ec-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="072ec-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="072ec-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="072ec-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="072ec-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="072ec-130">INPUTS</span></span>

### <span data-ttu-id="072ec-131">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="072ec-131">None</span></span>
<span data-ttu-id="072ec-132">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="072ec-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="072ec-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="072ec-133">OUTPUTS</span></span>

###  
<span data-ttu-id="072ec-134">Esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="072ec-134">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="072ec-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="072ec-135">NOTES</span></span>

## <span data-ttu-id="072ec-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="072ec-136">RELATED LINKS</span></span>

[<span data-ttu-id="072ec-137">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="072ec-137">Update-AzVmss</span></span>](./Update-AzVmss.md)


