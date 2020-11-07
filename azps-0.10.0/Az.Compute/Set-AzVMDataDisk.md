---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: C453485D-67A7-480E-83F6-527D4F5EBC93
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMDataDisk.md
ms.openlocfilehash: b927e9b61e4d76795e35f2356b900b959a94e082
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776833"
---
# <span data-ttu-id="38cb5-101">Set-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="38cb5-101">Set-AzVMDataDisk</span></span>

## <span data-ttu-id="38cb5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="38cb5-102">SYNOPSIS</span></span>
<span data-ttu-id="38cb5-103">Modifica as propriedades de um disco de dados da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="38cb5-103">Modifies properties of a virtual machine data disk.</span></span>

## <span data-ttu-id="38cb5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="38cb5-104">SYNTAX</span></span>

### <span data-ttu-id="38cb5-105">ChangeWithName</span><span class="sxs-lookup"><span data-stu-id="38cb5-105">ChangeWithName</span></span>
```
Set-AzVMDataDisk [-VM] <PSVirtualMachine> [-Name] <String> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-StorageAccountType <StorageAccountTypes>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38cb5-106">ChangeWithLun</span><span class="sxs-lookup"><span data-stu-id="38cb5-106">ChangeWithLun</span></span>
```
Set-AzVMDataDisk [-VM] <PSVirtualMachine> [-Lun] <Int32> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-StorageAccountType <StorageAccountTypes>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38cb5-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="38cb5-107">DESCRIPTION</span></span>
<span data-ttu-id="38cb5-108">O cmdlet **set-AzVMDataDisk** modifica as propriedades de um disco de dados de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="38cb5-108">The **Set-AzVMDataDisk** cmdlet modifies properties of a virtual machine data disk.</span></span>

## <span data-ttu-id="38cb5-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="38cb5-109">EXAMPLES</span></span>

### <span data-ttu-id="38cb5-110">Exemplo 1: modificar o modo de cache de um disco de dados</span><span class="sxs-lookup"><span data-stu-id="38cb5-110">Example 1: Modify the caching mode of a data disk</span></span>
```
PS C:\> $VM = Get-AzVM -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07"
PS C:\> Set-AzVMDataDisk -VM $VM -Name "DataDisk01" -Caching ReadWrite | Update-AzVM
```

<span data-ttu-id="38cb5-111">O primeiro comando obtém a máquina virtual chamada ContosoVM07 usando **Get-AzVM**.</span><span class="sxs-lookup"><span data-stu-id="38cb5-111">The first command gets the virtual machine named ContosoVM07 by using **Get-AzVM**.</span></span>
<span data-ttu-id="38cb5-112">O comando o armazena na variável $VM.</span><span class="sxs-lookup"><span data-stu-id="38cb5-112">The command stores it in the $VM variable.</span></span>

<span data-ttu-id="38cb5-113">O segundo comando modifica o modo de cache para o disco de dados chamado DataDisk01 na máquina virtual em $VM.</span><span class="sxs-lookup"><span data-stu-id="38cb5-113">The second command modifies the caching mode for the data disk named DataDisk01 on the virtual machine in $VM.</span></span>
<span data-ttu-id="38cb5-114">O comando passa o resultado para o cmdlet Update-AzVM, que implementa suas alterações.</span><span class="sxs-lookup"><span data-stu-id="38cb5-114">The command passes the result to the Update-AzVM cmdlet, which implements your changes.</span></span>
<span data-ttu-id="38cb5-115">Uma alteração no modo de pagamento faz com que a máquina virtual reinicie.</span><span class="sxs-lookup"><span data-stu-id="38cb5-115">A change to the cashing mode causes the virtual machine to restart.</span></span>

## <span data-ttu-id="38cb5-116">OS</span><span class="sxs-lookup"><span data-stu-id="38cb5-116">PARAMETERS</span></span>

### <span data-ttu-id="38cb5-117">-Cache</span><span class="sxs-lookup"><span data-stu-id="38cb5-117">-Caching</span></span>
<span data-ttu-id="38cb5-118">Especifica o modo de cache do disco.</span><span class="sxs-lookup"><span data-stu-id="38cb5-118">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="38cb5-119">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="38cb5-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="38cb5-120">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="38cb5-120">ReadOnly</span></span>
- <span data-ttu-id="38cb5-121">Leitura</span><span class="sxs-lookup"><span data-stu-id="38cb5-121">ReadWrite</span></span>

<span data-ttu-id="38cb5-122">O valor padrão é ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="38cb5-122">The default value is ReadWrite.</span></span>
<span data-ttu-id="38cb5-123">Alterar esse valor faz com que a máquina virtual seja reiniciada.</span><span class="sxs-lookup"><span data-stu-id="38cb5-123">Changing this value causes the virtual machine to restart.</span></span>

<span data-ttu-id="38cb5-124">Essa configuração afeta a consistência e o desempenho do disco.</span><span class="sxs-lookup"><span data-stu-id="38cb5-124">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="38cb5-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38cb5-125">-DefaultProfile</span></span>
<span data-ttu-id="38cb5-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="38cb5-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="38cb5-127">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="38cb5-127">-DiskSizeInGB</span></span>
<span data-ttu-id="38cb5-128">Especifica o tamanho, em gigabytes, para o disco de dados.</span><span class="sxs-lookup"><span data-stu-id="38cb5-128">Specifies the size, in gigabytes, for the data disk.</span></span>

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

### <span data-ttu-id="38cb5-129">-LUN</span><span class="sxs-lookup"><span data-stu-id="38cb5-129">-Lun</span></span>
<span data-ttu-id="38cb5-130">Especifica o número de unidade lógica (LUN) do disco de dados que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="38cb5-130">Specifies the logical unit number (LUN) of the data disk that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="38cb5-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="38cb5-131">-Name</span></span>
<span data-ttu-id="38cb5-132">Especifica o nome do disco de dados que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="38cb5-132">Specifies the name of the data disk that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="38cb5-133">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="38cb5-133">-StorageAccountType</span></span>
<span data-ttu-id="38cb5-134">O tipo de conta do disco gerenciado pela máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="38cb5-134">The virtual machine managed disk's account type.</span></span>

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

### <span data-ttu-id="38cb5-135">-VM</span><span class="sxs-lookup"><span data-stu-id="38cb5-135">-VM</span></span>
<span data-ttu-id="38cb5-136">Especifica a máquina virtual para a qual esse cmdlet modifica um disco de dados.</span><span class="sxs-lookup"><span data-stu-id="38cb5-136">Specifies the virtual machine for which this cmdlet modifies a data disk.</span></span>
<span data-ttu-id="38cb5-137">Para obter um objeto de máquina virtual, use o cmdlet Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="38cb5-137">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

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

### <span data-ttu-id="38cb5-138">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="38cb5-138">-WriteAccelerator</span></span>
<span data-ttu-id="38cb5-139">Especifica se o WriteAccelerator deve ser habilitado ou desabilitado no disco de dados.</span><span class="sxs-lookup"><span data-stu-id="38cb5-139">Specifies whether WriteAccelerator should be enabled or disabled on the data disk.</span></span>

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

### <span data-ttu-id="38cb5-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38cb5-140">CommonParameters</span></span>
<span data-ttu-id="38cb5-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38cb5-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38cb5-142">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38cb5-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38cb5-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="38cb5-143">INPUTS</span></span>

### <span data-ttu-id="38cb5-144">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="38cb5-144">PSVirtualMachine</span></span>
<span data-ttu-id="38cb5-145">O parâmetro ' VM ' aceita o valor do tipo ' PSVirtualMachine ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="38cb5-145">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="38cb5-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="38cb5-146">OUTPUTS</span></span>

### <span data-ttu-id="38cb5-147">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="38cb5-147">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="38cb5-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="38cb5-148">NOTES</span></span>

## <span data-ttu-id="38cb5-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="38cb5-149">RELATED LINKS</span></span>

[<span data-ttu-id="38cb5-150">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="38cb5-150">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="38cb5-151">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="38cb5-151">Update-AzVM</span></span>](./Update-AzVM.md)


