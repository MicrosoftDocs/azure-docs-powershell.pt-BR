---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: C453485D-67A7-480E-83F6-527D4F5EBC93
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRMVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRMVMDataDisk.md
ms.openlocfilehash: 4ed0abb355bf7a755e5acaa36f8bb11e88d80c5c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602626"
---
# <span data-ttu-id="a2c57-101">Set-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="a2c57-101">Set-AzureRmVMDataDisk</span></span>

## <span data-ttu-id="a2c57-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a2c57-102">SYNOPSIS</span></span>
<span data-ttu-id="a2c57-103">Modifica as propriedades de um disco de dados da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a2c57-103">Modifies properties of a virtual machine data disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a2c57-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a2c57-104">SYNTAX</span></span>

### <span data-ttu-id="a2c57-105">ChangeWithName</span><span class="sxs-lookup"><span data-stu-id="a2c57-105">ChangeWithName</span></span>
```
Set-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [-Name] <String> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-StorageAccountType <String>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2c57-106">ChangeWithLun</span><span class="sxs-lookup"><span data-stu-id="a2c57-106">ChangeWithLun</span></span>
```
Set-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [-Lun] <Int32> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-StorageAccountType <String>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2c57-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a2c57-107">DESCRIPTION</span></span>
<span data-ttu-id="a2c57-108">O cmdlet **set-AzureRmVMDataDisk** modifica as propriedades de um disco de dados de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a2c57-108">The **Set-AzureRmVMDataDisk** cmdlet modifies properties of a virtual machine data disk.</span></span>

## <span data-ttu-id="a2c57-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a2c57-109">EXAMPLES</span></span>

### <span data-ttu-id="a2c57-110">Exemplo 1: modificar o modo de cache de um disco de dados</span><span class="sxs-lookup"><span data-stu-id="a2c57-110">Example 1: Modify the caching mode of a data disk</span></span>
```
PS C:\> $VM = Get-AzureRMVM -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07"
PS C:\> Set-AzureRmVMDataDisk -VM $VM -Name "DataDisk01" -Caching ReadWrite | Update-AzureRmVM
```

<span data-ttu-id="a2c57-111">O primeiro comando obtém a máquina virtual chamada ContosoVM07 usando **Get-AzureRmVM**.</span><span class="sxs-lookup"><span data-stu-id="a2c57-111">The first command gets the virtual machine named ContosoVM07 by using **Get-AzureRmVM**.</span></span>
<span data-ttu-id="a2c57-112">O comando o armazena na variável $VM.</span><span class="sxs-lookup"><span data-stu-id="a2c57-112">The command stores it in the $VM variable.</span></span>
<span data-ttu-id="a2c57-113">O segundo comando modifica o modo de cache para o disco de dados chamado DataDisk01 na máquina virtual em $VM.</span><span class="sxs-lookup"><span data-stu-id="a2c57-113">The second command modifies the caching mode for the data disk named DataDisk01 on the virtual machine in $VM.</span></span>
<span data-ttu-id="a2c57-114">O comando passa o resultado para o cmdlet Update-AzureRmVM, que implementa suas alterações.</span><span class="sxs-lookup"><span data-stu-id="a2c57-114">The command passes the result to the Update-AzureRmVM cmdlet, which implements your changes.</span></span>
<span data-ttu-id="a2c57-115">Uma alteração no modo de pagamento faz com que a máquina virtual reinicie.</span><span class="sxs-lookup"><span data-stu-id="a2c57-115">A change to the cashing mode causes the virtual machine to restart.</span></span>

## <span data-ttu-id="a2c57-116">OS</span><span class="sxs-lookup"><span data-stu-id="a2c57-116">PARAMETERS</span></span>

### <span data-ttu-id="a2c57-117">-Cache</span><span class="sxs-lookup"><span data-stu-id="a2c57-117">-Caching</span></span>
<span data-ttu-id="a2c57-118">Especifica o modo de cache do disco.</span><span class="sxs-lookup"><span data-stu-id="a2c57-118">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="a2c57-119">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="a2c57-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a2c57-120">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="a2c57-120">ReadOnly</span></span>
- <span data-ttu-id="a2c57-121">ReadWrite o valor padrão é ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="a2c57-121">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="a2c57-122">Alterar esse valor faz com que a máquina virtual seja reiniciada.</span><span class="sxs-lookup"><span data-stu-id="a2c57-122">Changing this value causes the virtual machine to restart.</span></span>
<span data-ttu-id="a2c57-123">Essa configuração afeta a consistência e o desempenho do disco.</span><span class="sxs-lookup"><span data-stu-id="a2c57-123">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.CachingTypes]
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2c57-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2c57-124">-DefaultProfile</span></span>
<span data-ttu-id="a2c57-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a2c57-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2c57-126">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="a2c57-126">-DiskSizeInGB</span></span>
<span data-ttu-id="a2c57-127">Especifica o tamanho, em gigabytes, para o disco de dados.</span><span class="sxs-lookup"><span data-stu-id="a2c57-127">Specifies the size, in gigabytes, for the data disk.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2c57-128">-LUN</span><span class="sxs-lookup"><span data-stu-id="a2c57-128">-Lun</span></span>
<span data-ttu-id="a2c57-129">Especifica o número de unidade lógica (LUN) do disco de dados que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="a2c57-129">Specifies the logical unit number (LUN) of the data disk that this cmdlet modifies.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ChangeWithLun
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2c57-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="a2c57-130">-Name</span></span>
<span data-ttu-id="a2c57-131">Especifica o nome do disco de dados que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="a2c57-131">Specifies the name of the data disk that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ChangeWithName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2c57-132">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="a2c57-132">-StorageAccountType</span></span>
<span data-ttu-id="a2c57-133">O tipo de conta do disco gerenciado pela máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a2c57-133">The virtual machine managed disk's account type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2c57-134">-VM</span><span class="sxs-lookup"><span data-stu-id="a2c57-134">-VM</span></span>
<span data-ttu-id="a2c57-135">Especifica a máquina virtual para a qual esse cmdlet modifica um disco de dados.</span><span class="sxs-lookup"><span data-stu-id="a2c57-135">Specifies the virtual machine for which this cmdlet modifies a data disk.</span></span>
<span data-ttu-id="a2c57-136">Para obter um objeto de máquina virtual, use o cmdlet Get-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="a2c57-136">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a2c57-137">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="a2c57-137">-WriteAccelerator</span></span>
<span data-ttu-id="a2c57-138">Especifica se o WriteAccelerator deve ser habilitado ou desabilitado no disco de dados.</span><span class="sxs-lookup"><span data-stu-id="a2c57-138">Specifies whether WriteAccelerator should be enabled or disabled on the data disk.</span></span>

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

### <span data-ttu-id="a2c57-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2c57-139">CommonParameters</span></span>
<span data-ttu-id="a2c57-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2c57-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2c57-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2c57-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2c57-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a2c57-142">INPUTS</span></span>

### <span data-ttu-id="a2c57-143">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="a2c57-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="a2c57-144">System. String</span><span class="sxs-lookup"><span data-stu-id="a2c57-144">System.String</span></span>

### <span data-ttu-id="a2c57-145">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="a2c57-145">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="a2c57-146">System. Nullable ' 1 [[Microsoft. Azure. Management. COMPUTE. Models. CachingTypes, Microsoft. Azure. Management. Compute, Version = 21.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="a2c57-146">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=21.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="a2c57-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a2c57-147">OUTPUTS</span></span>

### <span data-ttu-id="a2c57-148">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="a2c57-148">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="a2c57-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a2c57-149">NOTES</span></span>

## <span data-ttu-id="a2c57-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a2c57-150">RELATED LINKS</span></span>

[<span data-ttu-id="a2c57-151">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a2c57-151">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="a2c57-152">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a2c57-152">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


