---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: C453485D-67A7-480E-83F6-527D4F5EBC93
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmdatadisk
schema: 2.0.0
ms.openlocfilehash: 53ad88f6e3df11eb3a8f2f9c4b21af40b9ea614b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786555"
---
# <span data-ttu-id="9f1e4-101">Set-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="9f1e4-101">Set-AzureRmVMDataDisk</span></span>

## <span data-ttu-id="9f1e4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9f1e4-102">SYNOPSIS</span></span>
<span data-ttu-id="9f1e4-103">Modifica as propriedades de um disco de dados da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9f1e4-103">Modifies properties of a virtual machine data disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9f1e4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9f1e4-104">SYNTAX</span></span>

### <span data-ttu-id="9f1e4-105">ChangeWithName</span><span class="sxs-lookup"><span data-stu-id="9f1e4-105">ChangeWithName</span></span>
```
Set-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [-Name] <String> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-StorageAccountType <StorageAccountTypes>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f1e4-106">ChangeWithLun</span><span class="sxs-lookup"><span data-stu-id="9f1e4-106">ChangeWithLun</span></span>
```
Set-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [-Lun] <Int32> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-StorageAccountType <StorageAccountTypes>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f1e4-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9f1e4-107">DESCRIPTION</span></span>
<span data-ttu-id="9f1e4-108">O cmdlet **set-AzureRmVMDataDisk** modifica as propriedades de um disco de dados de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9f1e4-108">The **Set-AzureRmVMDataDisk** cmdlet modifies properties of a virtual machine data disk.</span></span>

## <span data-ttu-id="9f1e4-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9f1e4-109">EXAMPLES</span></span>

### <span data-ttu-id="9f1e4-110">Exemplo 1: modificar o modo de cache de um disco de dados</span><span class="sxs-lookup"><span data-stu-id="9f1e4-110">Example 1: Modify the caching mode of a data disk</span></span>
```
PS C:\> $VM = Get-AzureRMVM -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07"
PS C:\> Set-AzureRmVMDataDisk -VM $VM -Name "DataDisk01" -Caching ReadWrite | Update-AzureRmVM
```

<span data-ttu-id="9f1e4-111">O primeiro comando obtém a máquina virtual chamada ContosoVM07 usando **Get-AzureRmVM**.</span><span class="sxs-lookup"><span data-stu-id="9f1e4-111">The first command gets the virtual machine named ContosoVM07 by using **Get-AzureRmVM**.</span></span>
<span data-ttu-id="9f1e4-112">O comando o armazena na variável $VM.</span><span class="sxs-lookup"><span data-stu-id="9f1e4-112">The command stores it in the $VM variable.</span></span>

<span data-ttu-id="9f1e4-113">O segundo comando modifica o modo de cache para o disco de dados chamado DataDisk01 na máquina virtual em $VM.</span><span class="sxs-lookup"><span data-stu-id="9f1e4-113">The second command modifies the caching mode for the data disk named DataDisk01 on the virtual machine in $VM.</span></span>
<span data-ttu-id="9f1e4-114">O comando passa o resultado para o cmdlet Update-AzureRmVM, que implementa suas alterações.</span><span class="sxs-lookup"><span data-stu-id="9f1e4-114">The command passes the result to the Update-AzureRmVM cmdlet, which implements your changes.</span></span>
<span data-ttu-id="9f1e4-115">Uma alteração no modo de pagamento faz com que a máquina virtual reinicie.</span><span class="sxs-lookup"><span data-stu-id="9f1e4-115">A change to the cashing mode causes the virtual machine to restart.</span></span>

## <span data-ttu-id="9f1e4-116">OS</span><span class="sxs-lookup"><span data-stu-id="9f1e4-116">PARAMETERS</span></span>

### <span data-ttu-id="9f1e4-117">-Cache</span><span class="sxs-lookup"><span data-stu-id="9f1e4-117">-Caching</span></span>
<span data-ttu-id="9f1e4-118">Especifica o modo de cache do disco.</span><span class="sxs-lookup"><span data-stu-id="9f1e4-118">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="9f1e4-119">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="9f1e4-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9f1e4-120">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="9f1e4-120">ReadOnly</span></span>
- <span data-ttu-id="9f1e4-121">Leitura</span><span class="sxs-lookup"><span data-stu-id="9f1e4-121">ReadWrite</span></span>

<span data-ttu-id="9f1e4-122">O valor padrão é ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="9f1e4-122">The default value is ReadWrite.</span></span>
<span data-ttu-id="9f1e4-123">Alterar esse valor faz com que a máquina virtual seja reiniciada.</span><span class="sxs-lookup"><span data-stu-id="9f1e4-123">Changing this value causes the virtual machine to restart.</span></span>

<span data-ttu-id="9f1e4-124">Essa configuração afeta a consistência e o desempenho do disco.</span><span class="sxs-lookup"><span data-stu-id="9f1e4-124">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: CachingTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f1e4-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f1e4-125">-DefaultProfile</span></span>
<span data-ttu-id="9f1e4-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9f1e4-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9f1e4-127">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="9f1e4-127">-DiskSizeInGB</span></span>
<span data-ttu-id="9f1e4-128">Especifica o tamanho, em gigabytes, para o disco de dados.</span><span class="sxs-lookup"><span data-stu-id="9f1e4-128">Specifies the size, in gigabytes, for the data disk.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f1e4-129">-LUN</span><span class="sxs-lookup"><span data-stu-id="9f1e4-129">-Lun</span></span>
<span data-ttu-id="9f1e4-130">Especifica o número de unidade lógica (LUN) do disco de dados que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="9f1e4-130">Specifies the logical unit number (LUN) of the data disk that this cmdlet modifies.</span></span>

```yaml
Type: Int32
Parameter Sets: ChangeWithLun
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f1e4-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="9f1e4-131">-Name</span></span>
<span data-ttu-id="9f1e4-132">Especifica o nome do disco de dados que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="9f1e4-132">Specifies the name of the data disk that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: ChangeWithName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f1e4-133">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="9f1e4-133">-StorageAccountType</span></span>
<span data-ttu-id="9f1e4-134">O tipo de conta do disco gerenciado pela máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9f1e4-134">The virtual machine managed disk's account type.</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: 
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f1e4-135">-VM</span><span class="sxs-lookup"><span data-stu-id="9f1e4-135">-VM</span></span>
<span data-ttu-id="9f1e4-136">Especifica a máquina virtual para a qual esse cmdlet modifica um disco de dados.</span><span class="sxs-lookup"><span data-stu-id="9f1e4-136">Specifies the virtual machine for which this cmdlet modifies a data disk.</span></span>
<span data-ttu-id="9f1e4-137">Para obter um objeto de máquina virtual, use o cmdlet Get-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="9f1e4-137">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9f1e4-138">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="9f1e4-138">-WriteAccelerator</span></span>
<span data-ttu-id="9f1e4-139">Especifica se o WriteAccelerator deve ser habilitado ou desabilitado no disco de dados.</span><span class="sxs-lookup"><span data-stu-id="9f1e4-139">Specifies whether WriteAccelerator should be enabled or disabled on the data disk.</span></span>

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

### <span data-ttu-id="9f1e4-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f1e4-140">CommonParameters</span></span>
<span data-ttu-id="9f1e4-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f1e4-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f1e4-142">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f1e4-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f1e4-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9f1e4-143">INPUTS</span></span>

### <span data-ttu-id="9f1e4-144">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="9f1e4-144">PSVirtualMachine</span></span>
<span data-ttu-id="9f1e4-145">O parâmetro ' VM ' aceita o valor do tipo ' PSVirtualMachine ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="9f1e4-145">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="9f1e4-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9f1e4-146">OUTPUTS</span></span>

### <span data-ttu-id="9f1e4-147">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="9f1e4-147">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="9f1e4-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9f1e4-148">NOTES</span></span>

## <span data-ttu-id="9f1e4-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9f1e4-149">RELATED LINKS</span></span>

[<span data-ttu-id="9f1e4-150">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="9f1e4-150">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="9f1e4-151">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="9f1e4-151">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


