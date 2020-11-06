---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: C453485D-67A7-480E-83F6-527D4F5EBC93
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRMVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRMVMDataDisk.md
ms.openlocfilehash: 3bc870be1628f5fbf22042155e6a889dbdaadc84
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602063"
---
# <span data-ttu-id="8a376-101">Set-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="8a376-101">Set-AzureRmVMDataDisk</span></span>

## <span data-ttu-id="8a376-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8a376-102">SYNOPSIS</span></span>
<span data-ttu-id="8a376-103">Modifica as propriedades de um disco de dados da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8a376-103">Modifies properties of a virtual machine data disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8a376-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8a376-104">SYNTAX</span></span>

### <span data-ttu-id="8a376-105">ChangeWithName</span><span class="sxs-lookup"><span data-stu-id="8a376-105">ChangeWithName</span></span>
```
Set-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [-Name] <String> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-StorageAccountType <StorageAccountTypes>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8a376-106">ChangeWithLun</span><span class="sxs-lookup"><span data-stu-id="8a376-106">ChangeWithLun</span></span>
```
Set-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [-Lun] <Int32> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-StorageAccountType <StorageAccountTypes>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8a376-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8a376-107">DESCRIPTION</span></span>
<span data-ttu-id="8a376-108">O cmdlet **set-AzureRmVMDataDisk** modifica as propriedades de um disco de dados de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8a376-108">The **Set-AzureRmVMDataDisk** cmdlet modifies properties of a virtual machine data disk.</span></span>

## <span data-ttu-id="8a376-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8a376-109">EXAMPLES</span></span>

### <span data-ttu-id="8a376-110">Exemplo 1: modificar o modo de cache de um disco de dados</span><span class="sxs-lookup"><span data-stu-id="8a376-110">Example 1: Modify the caching mode of a data disk</span></span>
```
PS C:\> $VM = Get-AzureRMVM -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07"
PS C:\> Set-AzureRmVMDataDisk -VM $VM -Name "DataDisk01" -Caching ReadWrite | Update-AzureRmVM
```

<span data-ttu-id="8a376-111">O primeiro comando obtém a máquina virtual chamada ContosoVM07 usando **Get-AzureRmVM**.</span><span class="sxs-lookup"><span data-stu-id="8a376-111">The first command gets the virtual machine named ContosoVM07 by using **Get-AzureRmVM**.</span></span>
<span data-ttu-id="8a376-112">O comando o armazena na variável $VM.</span><span class="sxs-lookup"><span data-stu-id="8a376-112">The command stores it in the $VM variable.</span></span>

<span data-ttu-id="8a376-113">O segundo comando modifica o modo de cache para o disco de dados chamado DataDisk01 na máquina virtual em $VM.</span><span class="sxs-lookup"><span data-stu-id="8a376-113">The second command modifies the caching mode for the data disk named DataDisk01 on the virtual machine in $VM.</span></span>
<span data-ttu-id="8a376-114">O comando passa o resultado para o cmdlet Update-AzureRmVM, que implementa suas alterações.</span><span class="sxs-lookup"><span data-stu-id="8a376-114">The command passes the result to the Update-AzureRmVM cmdlet, which implements your changes.</span></span>
<span data-ttu-id="8a376-115">Uma alteração no modo de pagamento faz com que a máquina virtual reinicie.</span><span class="sxs-lookup"><span data-stu-id="8a376-115">A change to the cashing mode causes the virtual machine to restart.</span></span>

## <span data-ttu-id="8a376-116">OS</span><span class="sxs-lookup"><span data-stu-id="8a376-116">PARAMETERS</span></span>

### <span data-ttu-id="8a376-117">-Cache</span><span class="sxs-lookup"><span data-stu-id="8a376-117">-Caching</span></span>
<span data-ttu-id="8a376-118">Especifica o modo de cache do disco.</span><span class="sxs-lookup"><span data-stu-id="8a376-118">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="8a376-119">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="8a376-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8a376-120">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="8a376-120">ReadOnly</span></span>
- <span data-ttu-id="8a376-121">Leitura</span><span class="sxs-lookup"><span data-stu-id="8a376-121">ReadWrite</span></span>

<span data-ttu-id="8a376-122">O valor padrão é ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="8a376-122">The default value is ReadWrite.</span></span>
<span data-ttu-id="8a376-123">Alterar esse valor faz com que a máquina virtual seja reiniciada.</span><span class="sxs-lookup"><span data-stu-id="8a376-123">Changing this value causes the virtual machine to restart.</span></span>

<span data-ttu-id="8a376-124">Essa configuração afeta a consistência e o desempenho do disco.</span><span class="sxs-lookup"><span data-stu-id="8a376-124">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="8a376-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a376-125">-DefaultProfile</span></span>
<span data-ttu-id="8a376-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8a376-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a376-127">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="8a376-127">-DiskSizeInGB</span></span>
<span data-ttu-id="8a376-128">Especifica o tamanho, em gigabytes, para o disco de dados.</span><span class="sxs-lookup"><span data-stu-id="8a376-128">Specifies the size, in gigabytes, for the data disk.</span></span>

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

### <span data-ttu-id="8a376-129">-LUN</span><span class="sxs-lookup"><span data-stu-id="8a376-129">-Lun</span></span>
<span data-ttu-id="8a376-130">Especifica o número de unidade lógica (LUN) do disco de dados que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="8a376-130">Specifies the logical unit number (LUN) of the data disk that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="8a376-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="8a376-131">-Name</span></span>
<span data-ttu-id="8a376-132">Especifica o nome do disco de dados que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="8a376-132">Specifies the name of the data disk that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="8a376-133">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="8a376-133">-StorageAccountType</span></span>
<span data-ttu-id="8a376-134">O tipo de conta do disco gerenciado pela máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8a376-134">The virtual machine managed disk's account type.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.StorageAccountTypes]
Parameter Sets: (All)
Aliases: 
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a376-135">-VM</span><span class="sxs-lookup"><span data-stu-id="8a376-135">-VM</span></span>
<span data-ttu-id="8a376-136">Especifica a máquina virtual para a qual esse cmdlet modifica um disco de dados.</span><span class="sxs-lookup"><span data-stu-id="8a376-136">Specifies the virtual machine for which this cmdlet modifies a data disk.</span></span>
<span data-ttu-id="8a376-137">Para obter um objeto de máquina virtual, use o cmdlet Get-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="8a376-137">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

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

### <span data-ttu-id="8a376-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a376-138">CommonParameters</span></span>
<span data-ttu-id="8a376-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a376-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a376-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a376-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a376-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8a376-141">INPUTS</span></span>

## <span data-ttu-id="8a376-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8a376-142">OUTPUTS</span></span>

## <span data-ttu-id="8a376-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8a376-143">NOTES</span></span>

## <span data-ttu-id="8a376-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8a376-144">RELATED LINKS</span></span>

[<span data-ttu-id="8a376-145">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="8a376-145">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="8a376-146">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="8a376-146">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


