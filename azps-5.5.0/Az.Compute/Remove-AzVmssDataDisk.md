---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssDataDisk.md
ms.openlocfilehash: 908405de847526682d8526ef2e576e6a07893c3a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112105"
---
# <span data-ttu-id="541ef-101">Remove-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="541ef-101">Remove-AzVmssDataDisk</span></span>

## <span data-ttu-id="541ef-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="541ef-102">SYNOPSIS</span></span>
<span data-ttu-id="541ef-103">Remove um disco de dados do VMSS.</span><span class="sxs-lookup"><span data-stu-id="541ef-103">Removes a data disk from the VMSS.</span></span>

## <span data-ttu-id="541ef-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="541ef-104">SYNTAX</span></span>

### <span data-ttu-id="541ef-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="541ef-105">NameParameterSet</span></span>
```
Remove-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="541ef-106">InstoTomParameterSet</span><span class="sxs-lookup"><span data-stu-id="541ef-106">LunParameterSet</span></span>
```
Remove-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Lun] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="541ef-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="541ef-107">DESCRIPTION</span></span>
<span data-ttu-id="541ef-108">O cmdlet **Remove-AzVmssDataDisk** remove um disco de dados da instância VMSS (Virtual Machine Scale Set).</span><span class="sxs-lookup"><span data-stu-id="541ef-108">The **Remove-AzVmssDataDisk** cmdlet removes a data disk from the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="541ef-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="541ef-109">EXAMPLES</span></span>

### <span data-ttu-id="541ef-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="541ef-110">Example 1</span></span>
```
PS C:\> Remove-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1'
```

<span data-ttu-id="541ef-111">Esse comando remove o disco de dados chamado 'DataDisk1' do objeto VMSS.</span><span class="sxs-lookup"><span data-stu-id="541ef-111">This command removes the data disk named 'DataDisk1' from the VMSS object.</span></span>

### <span data-ttu-id="541ef-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="541ef-112">Example 2</span></span>
```
PS C:\> Remove-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Lun 0
```

<span data-ttu-id="541ef-113">Esse comando remove o disco de dados de OBJECT 0 do objeto VMSS.</span><span class="sxs-lookup"><span data-stu-id="541ef-113">This command removes the data disk of LUN 0 from the VMSS object.</span></span>

## <span data-ttu-id="541ef-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="541ef-114">PARAMETERS</span></span>

### <span data-ttu-id="541ef-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="541ef-115">-DefaultProfile</span></span>
<span data-ttu-id="541ef-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="541ef-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="541ef-117">-Ltda</span><span class="sxs-lookup"><span data-stu-id="541ef-117">-Lun</span></span>
<span data-ttu-id="541ef-118">Especifica o número da unidade lógica do disco.</span><span class="sxs-lookup"><span data-stu-id="541ef-118">Specifies the logical unit number of the disk.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: LunParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="541ef-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="541ef-119">-Name</span></span>
<span data-ttu-id="541ef-120">Especifica o nome do disco.</span><span class="sxs-lookup"><span data-stu-id="541ef-120">Specifies the name of the disk.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="541ef-121">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="541ef-121">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="541ef-122">Especifique o objeto VMSS.</span><span class="sxs-lookup"><span data-stu-id="541ef-122">Specify the VMSS object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="541ef-123">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="541ef-123">-Confirm</span></span>
<span data-ttu-id="541ef-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="541ef-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="541ef-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="541ef-125">-WhatIf</span></span>
<span data-ttu-id="541ef-126">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="541ef-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="541ef-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="541ef-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="541ef-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="541ef-128">CommonParameters</span></span>
<span data-ttu-id="541ef-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="541ef-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="541ef-130">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="541ef-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="541ef-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="541ef-131">INPUTS</span></span>

### <span data-ttu-id="541ef-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="541ef-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="541ef-133">System.String</span><span class="sxs-lookup"><span data-stu-id="541ef-133">System.String</span></span>

### <span data-ttu-id="541ef-134">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="541ef-134">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="541ef-135">Saídas</span><span class="sxs-lookup"><span data-stu-id="541ef-135">OUTPUTS</span></span>

### <span data-ttu-id="541ef-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="541ef-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="541ef-137">Notas</span><span class="sxs-lookup"><span data-stu-id="541ef-137">NOTES</span></span>

## <span data-ttu-id="541ef-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="541ef-138">RELATED LINKS</span></span>
