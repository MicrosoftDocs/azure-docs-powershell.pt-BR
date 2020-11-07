---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: FDEDBF4F-7507-43FF-A983-7E431C0C1950
online version: ''
schema: 2.0.0
ms.openlocfilehash: 967fbaf83efa12bd305fc9fe075a9abffdd62dc3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945735"
---
# <span data-ttu-id="591c0-101">Add-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="591c0-101">Add-AzureDataDisk</span></span>

## <span data-ttu-id="591c0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="591c0-102">SYNOPSIS</span></span>
<span data-ttu-id="591c0-103">Adiciona um disco de dados a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="591c0-103">Adds a data disk to a virtual machine.</span></span>

## <span data-ttu-id="591c0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="591c0-104">SYNTAX</span></span>

### <span data-ttu-id="591c0-105">CreateNew (padrão)</span><span class="sxs-lookup"><span data-stu-id="591c0-105">CreateNew (Default)</span></span>
```
Add-AzureDataDisk [-CreateNew] [-DiskSizeInGB] <Int32> [-DiskLabel] <String> [-LUN] <Int32>
 [-MediaLocation <String>] [-HostCaching <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="591c0-106">Importações</span><span class="sxs-lookup"><span data-stu-id="591c0-106">Import</span></span>
```
Add-AzureDataDisk [-Import] [-DiskName] <String> [-LUN] <Int32> [-HostCaching <String>] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="591c0-107">ImportFrom</span><span class="sxs-lookup"><span data-stu-id="591c0-107">ImportFrom</span></span>
```
Add-AzureDataDisk [-ImportFrom] [-DiskLabel] <String> [-LUN] <Int32> -MediaLocation <String>
 [-HostCaching <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="591c0-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="591c0-108">DESCRIPTION</span></span>
<span data-ttu-id="591c0-109">O cmdlet **Add-AzureDataDisk** adiciona um disco de dados novo ou existente a um objeto de máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="591c0-109">The **Add-AzureDataDisk** cmdlet adds a new or existing data disk to an Azure virtual machine object.</span></span>
<span data-ttu-id="591c0-110">Use o parâmetro *CreateNew* para criar um novo disco de dados que tenha um tamanho e um rótulo especificados.</span><span class="sxs-lookup"><span data-stu-id="591c0-110">Use the *CreateNew* parameter to create a new data disk that has a specified size and label.</span></span>
<span data-ttu-id="591c0-111">Use o parâmetro de *importação* para anexar um disco existente do repositório de imagens.</span><span class="sxs-lookup"><span data-stu-id="591c0-111">Use the *Import* parameter to attach an existing disk from the image repository.</span></span>
<span data-ttu-id="591c0-112">Use o parâmetro *ImportFrom* para anexar um disco existente de um blob em uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="591c0-112">Use the *ImportFrom* parameter to attach an existing disk from a blob in a storage account.</span></span>
<span data-ttu-id="591c0-113">Você pode especificar o modo de cache do host do disco de dados anexado.</span><span class="sxs-lookup"><span data-stu-id="591c0-113">You can specify the host-cache mode of the attached data disk.</span></span>

## <span data-ttu-id="591c0-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="591c0-114">EXAMPLES</span></span>

### <span data-ttu-id="591c0-115">Exemplo 1: importar um disco de dados do repositório</span><span class="sxs-lookup"><span data-stu-id="591c0-115">Example 1: Import a data disk from the repository</span></span>
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine07" | Add-AzureDataDisk -Import -DiskName "Disk68" -LUN 0 | Update-AzureVM
```

<span data-ttu-id="591c0-116">Este comando obtém um objeto de máquina virtual para a máquina virtual nomeada VirtualMachine07 no serviço de nuvem do ContosoService usando o cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="591c0-116">This command gets a virtual machine object for the virtual machine named VirtualMachine07 in the ContosoService cloud service by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="591c0-117">O comando passa a ele para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="591c0-117">The command passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="591c0-118">Esse comando anexa um disco de dados existente do repositório à máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="591c0-118">That command attaches an existing data disk from the repository to the virtual machine.</span></span>
<span data-ttu-id="591c0-119">O disco de dados tem um LUN de 0.</span><span class="sxs-lookup"><span data-stu-id="591c0-119">The data disk has a LUN of 0.</span></span>
<span data-ttu-id="591c0-120">O comando atualiza a máquina virtual para refletir suas alterações usando o cmdlet **Update-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="591c0-120">The command updates the virtual machine to reflect your changes by using the **Update-AzureVM** cmdlet.</span></span>

### <span data-ttu-id="591c0-121">Exemplo 2: adicionar um novo disco de dados</span><span class="sxs-lookup"><span data-stu-id="591c0-121">Example 2: Add a new data disk</span></span>
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine08" | Add-AzureDataDisk -CreateNew -DiskSizeInGB 128 -DiskLabel "main" -LUN 0 | Update-AzureVM
```

<span data-ttu-id="591c0-122">Este comando obtém um objeto da máquina virtual para a máquina virtual chamada VirtualMachine08.</span><span class="sxs-lookup"><span data-stu-id="591c0-122">This command gets a virtual machine object for the virtual machine named VirtualMachine08.</span></span>
<span data-ttu-id="591c0-123">O comando a passa para o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="591c0-123">The command passes it to the current cmdlet.</span></span>
<span data-ttu-id="591c0-124">Esse comando anexa um novo disco de dados chamado MyNewDisk. vhd.</span><span class="sxs-lookup"><span data-stu-id="591c0-124">That command attaches a new data disk named MyNewDisk.vhd.</span></span>
<span data-ttu-id="591c0-125">O cmdlet cria o disco no contêiner VHDs na conta de armazenamento padrão da assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="591c0-125">The cmdlet creates the disk in the vhds container in the default storage account of the current subscription.</span></span>
<span data-ttu-id="591c0-126">O comando atualiza a máquina virtual para refletir suas alterações.</span><span class="sxs-lookup"><span data-stu-id="591c0-126">The command updates the virtual machine to reflect your changes.</span></span>

### <span data-ttu-id="591c0-127">Exemplo 3: adicionar um disco de dados de um local especificado</span><span class="sxs-lookup"><span data-stu-id="591c0-127">Example 3: Add a data disk from a specified location</span></span>
```
PS C:\> Get-AzureVM "ContosoService" -Name "Database" | Add-AzureDataDisk -ImportFrom -MediaLocation "https://contosostorage.blob.core.windows.net/container07/Disk14.vhd" -DiskLabel "main" -LUN 0 | Update-AzureVM
```

<span data-ttu-id="591c0-128">Este comando obtém um objeto de máquina virtual para a máquina virtual nomeada banco de dados.</span><span class="sxs-lookup"><span data-stu-id="591c0-128">This command gets a virtual machine object for the virtual machine named Database.</span></span>
<span data-ttu-id="591c0-129">O comando a passa para o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="591c0-129">The command passes it to the current cmdlet.</span></span>
<span data-ttu-id="591c0-130">Esse comando anexa um disco de dados existente chamado Disk14. vhd do local especificado.</span><span class="sxs-lookup"><span data-stu-id="591c0-130">That command attaches an existing data disk named Disk14.vhd from the specified location.</span></span>
<span data-ttu-id="591c0-131">O comando atualiza a máquina virtual para refletir suas alterações.</span><span class="sxs-lookup"><span data-stu-id="591c0-131">The command updates the virtual machine to reflect your changes.</span></span>

## <span data-ttu-id="591c0-132">OS</span><span class="sxs-lookup"><span data-stu-id="591c0-132">PARAMETERS</span></span>

### <span data-ttu-id="591c0-133">-CreateNew</span><span class="sxs-lookup"><span data-stu-id="591c0-133">-CreateNew</span></span>
<span data-ttu-id="591c0-134">Indica que esse cmdlet cria um disco de dados.</span><span class="sxs-lookup"><span data-stu-id="591c0-134">Indicates that this cmdlet creates a data disk.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: CreateNew
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="591c0-135">-DiskLabel</span><span class="sxs-lookup"><span data-stu-id="591c0-135">-DiskLabel</span></span>
<span data-ttu-id="591c0-136">Especifica o rótulo de disco para um novo disco de dados.</span><span class="sxs-lookup"><span data-stu-id="591c0-136">Specifies the disk label for a new data disk.</span></span>

```yaml
Type: String
Parameter Sets: CreateNew, ImportFrom
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="591c0-137">-Diskname</span><span class="sxs-lookup"><span data-stu-id="591c0-137">-DiskName</span></span>
<span data-ttu-id="591c0-138">Especifica o nome de um disco de dados no repositório de discos.</span><span class="sxs-lookup"><span data-stu-id="591c0-138">Specifies the name of a data disk in the disk repository.</span></span>

```yaml
Type: String
Parameter Sets: Import
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="591c0-139">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="591c0-139">-DiskSizeInGB</span></span>
<span data-ttu-id="591c0-140">Especifica o tamanho do disco lógico, em gigabytes, para um novo disco de dados.</span><span class="sxs-lookup"><span data-stu-id="591c0-140">Specifies the logical disk size, in gigabytes, for a new data disk.</span></span>

```yaml
Type: Int32
Parameter Sets: CreateNew
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="591c0-141">-HostCaching</span><span class="sxs-lookup"><span data-stu-id="591c0-141">-HostCaching</span></span>
<span data-ttu-id="591c0-142">Especifica as configurações de cache do nível do host do disco.</span><span class="sxs-lookup"><span data-stu-id="591c0-142">Specifies the host level caching settings of the disk.</span></span>
<span data-ttu-id="591c0-143">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="591c0-143">Valid values are:</span></span> 

- <span data-ttu-id="591c0-144">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="591c0-144">None</span></span> 
- <span data-ttu-id="591c0-145">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="591c0-145">ReadOnly</span></span> 
- <span data-ttu-id="591c0-146">Leitura</span><span class="sxs-lookup"><span data-stu-id="591c0-146">ReadWrite</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="591c0-147">-Importar</span><span class="sxs-lookup"><span data-stu-id="591c0-147">-Import</span></span>
<span data-ttu-id="591c0-148">Indica que esse cmdlet importa um disco de dados existente do repositório de imagens.</span><span class="sxs-lookup"><span data-stu-id="591c0-148">Indicates that this cmdlet imports an existing data disk from the image repository.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Import
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="591c0-149">-ImportFrom</span><span class="sxs-lookup"><span data-stu-id="591c0-149">-ImportFrom</span></span>
<span data-ttu-id="591c0-150">Indica que esse cmdlet importa um disco de dados existente de um blob em uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="591c0-150">Indicates that this cmdlet imports an existing data disk from a blob in a storage account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ImportFrom
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="591c0-151">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="591c0-151">-InformationAction</span></span>
<span data-ttu-id="591c0-152">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="591c0-152">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="591c0-153">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="591c0-153">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="591c0-154">Contínuo</span><span class="sxs-lookup"><span data-stu-id="591c0-154">Continue</span></span>
- <span data-ttu-id="591c0-155">Ignorar</span><span class="sxs-lookup"><span data-stu-id="591c0-155">Ignore</span></span>
- <span data-ttu-id="591c0-156">Inquire</span><span class="sxs-lookup"><span data-stu-id="591c0-156">Inquire</span></span>
- <span data-ttu-id="591c0-157">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="591c0-157">SilentlyContinue</span></span>
- <span data-ttu-id="591c0-158">Finaliza</span><span class="sxs-lookup"><span data-stu-id="591c0-158">Stop</span></span>
- <span data-ttu-id="591c0-159">Suspensão</span><span class="sxs-lookup"><span data-stu-id="591c0-159">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="591c0-160">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="591c0-160">-InformationVariable</span></span>
<span data-ttu-id="591c0-161">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="591c0-161">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="591c0-162">-LUN</span><span class="sxs-lookup"><span data-stu-id="591c0-162">-LUN</span></span>
<span data-ttu-id="591c0-163">Especifica o número de unidade lógica (LUN) para a unidade de dados na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="591c0-163">Specifies the logical unit number (LUN) for the data drive in the virtual machine.</span></span>
<span data-ttu-id="591c0-164">Os valores válidos são: de 0 a 15.</span><span class="sxs-lookup"><span data-stu-id="591c0-164">Valid values are: 0 through 15.</span></span>
<span data-ttu-id="591c0-165">Cada disco de dados deve ter um LUN exclusivo.</span><span class="sxs-lookup"><span data-stu-id="591c0-165">Each data disk must have a unique LUN.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="591c0-166">-MediaLocation</span><span class="sxs-lookup"><span data-stu-id="591c0-166">-MediaLocation</span></span>
<span data-ttu-id="591c0-167">Especifica o local do blob em uma conta de armazenamento do Azure na qual esse cmdlet armazena o disco de dados.</span><span class="sxs-lookup"><span data-stu-id="591c0-167">Specifies the location of the blob in an Azure storage account where this cmdlet stores the data disk.</span></span>
<span data-ttu-id="591c0-168">Se você não especificar um local, o cmdlet armazenará o disco de dados no contêiner VHDs na conta de armazenamento padrão para a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="591c0-168">If you do not specify a location, the cmdlet stores the data disk in the vhds container in the default storage account for the current subscription.</span></span>
<span data-ttu-id="591c0-169">Se um contêiner de VHDs não existir, o cmdlet criará um contêiner de VHDs.</span><span class="sxs-lookup"><span data-stu-id="591c0-169">If a vhds container does not exist, the cmdlet creates a vhds container.</span></span>

```yaml
Type: String
Parameter Sets: CreateNew
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ImportFrom
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="591c0-170">-Perfil</span><span class="sxs-lookup"><span data-stu-id="591c0-170">-Profile</span></span>
<span data-ttu-id="591c0-171">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="591c0-171">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="591c0-172">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="591c0-172">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="591c0-173">-VM</span><span class="sxs-lookup"><span data-stu-id="591c0-173">-VM</span></span>
<span data-ttu-id="591c0-174">Especifica o objeto da máquina virtual para o qual esse cmdlet anexa um disco de dados.</span><span class="sxs-lookup"><span data-stu-id="591c0-174">Specifies the virtual machine object to which this cmdlet attaches a data disk.</span></span>
<span data-ttu-id="591c0-175">Para obter um objeto de máquina virtual, use o cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="591c0-175">To obtain a virtual machine object, use the **Get-AzureVM** cmdlet.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="591c0-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="591c0-176">CommonParameters</span></span>
<span data-ttu-id="591c0-177">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="591c0-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="591c0-178">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="591c0-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="591c0-179">SENSORES</span><span class="sxs-lookup"><span data-stu-id="591c0-179">INPUTS</span></span>

## <span data-ttu-id="591c0-180">EXIBE</span><span class="sxs-lookup"><span data-stu-id="591c0-180">OUTPUTS</span></span>

## <span data-ttu-id="591c0-181">INFORMA</span><span class="sxs-lookup"><span data-stu-id="591c0-181">NOTES</span></span>

## <span data-ttu-id="591c0-182">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="591c0-182">RELATED LINKS</span></span>

[<span data-ttu-id="591c0-183">Get-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="591c0-183">Get-AzureDataDisk</span></span>](./Get-AzureDataDisk.md)

[<span data-ttu-id="591c0-184">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="591c0-184">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="591c0-185">Remove-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="591c0-185">Remove-AzureDataDisk</span></span>](./Remove-AzureDataDisk.md)

[<span data-ttu-id="591c0-186">Set-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="591c0-186">Set-AzureDataDisk</span></span>](./Set-AzureDataDisk.md)

[<span data-ttu-id="591c0-187">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="591c0-187">Update-AzureVM</span></span>](./Update-AzureVM.md)


