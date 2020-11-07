---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: D563ACF6-6BCD-4463-8731-175BA047A74D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2ceb2af6b359d5b9660397ef654d6c56e045ce64
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946166"
---
# <span data-ttu-id="763b5-101">Remove-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="763b5-101">Remove-AzureDataDisk</span></span>

## <span data-ttu-id="763b5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="763b5-102">SYNOPSIS</span></span>
<span data-ttu-id="763b5-103">Remove um disco de dados de uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="763b5-103">Removes a data disk from an Azure virtual machine.</span></span>

## <span data-ttu-id="763b5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="763b5-104">SYNTAX</span></span>

```
Remove-AzureDataDisk [-LUN] <Int32> [-DeleteVHD] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="763b5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="763b5-105">DESCRIPTION</span></span>
<span data-ttu-id="763b5-106">O cmdlet **Remove-AzureDataDisk** remove um disco de dados de uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="763b5-106">The **Remove-AzureDataDisk** cmdlet removes a data disk from an Azure virtual machine.</span></span>
<span data-ttu-id="763b5-107">Por padrão, esse cmdlet não remove o blob do disco de dados da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="763b5-107">By default, this cmdlet does not remove the data disk blob from the storage account.</span></span>

## <span data-ttu-id="763b5-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="763b5-108">EXAMPLES</span></span>

### <span data-ttu-id="763b5-109">Exemplo 1: remover um disco de dados</span><span class="sxs-lookup"><span data-stu-id="763b5-109">Example 1: Remove a data disk</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Remove-AzureDataDisk -LUN 0
```

<span data-ttu-id="763b5-110">Esse comando obtém a máquina virtual chamada VirtualMachine07 no serviço chamado ContosoService usando o cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="763b5-110">This command gets the virtual machine named VirtualMachine07 in the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="763b5-111">O comando passa a máquina virtual para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="763b5-111">The command passes the virtual machine to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="763b5-112">O cmdlet atual remove o disco de dados que tem o LUN 0.</span><span class="sxs-lookup"><span data-stu-id="763b5-112">The current cmdlet removes the data disk that has the LUN 0.</span></span>

### <span data-ttu-id="763b5-113">Exemplo 2: remover um disco de dados e o arquivo de disco rígido virtual</span><span class="sxs-lookup"><span data-stu-id="763b5-113">Example 2: Remove a data disk and the virtual hard disk file</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Remove-AzureDataDisk -LUN 0 -DeleteVHD | Update-AzureVM
```

<span data-ttu-id="763b5-114">Esse comando obtém a máquina virtual chamada VirtualMachine07 no serviço chamado ContosoService.</span><span class="sxs-lookup"><span data-stu-id="763b5-114">This command gets the virtual machine named VirtualMachine07 in the service named ContosoService.</span></span>
<span data-ttu-id="763b5-115">O comando passa a máquina virtual para o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="763b5-115">The command passes the virtual machine to the current cmdlet.</span></span>
<span data-ttu-id="763b5-116">O cmdlet atual remove o disco de dados que tem o LUN 0.</span><span class="sxs-lookup"><span data-stu-id="763b5-116">The current cmdlet removes the data disk that has the LUN 0.</span></span>
<span data-ttu-id="763b5-117">O comando inclui o parâmetro *DeleteVHD* .</span><span class="sxs-lookup"><span data-stu-id="763b5-117">The command includes the *DeleteVHD* parameter.</span></span>
<span data-ttu-id="763b5-118">Portanto, ele também exclui o disco rígido virtual subjacente.</span><span class="sxs-lookup"><span data-stu-id="763b5-118">Therefore, it also deletes the underlying virtual hard disk.</span></span>
<span data-ttu-id="763b5-119">O comando atualiza a máquina virtual para refletir suas alterações usando o cmdlet **Update-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="763b5-119">The command updates the virtual machine to reflect your changes by using the **Update-AzureVM** cmdlet.</span></span>

## <span data-ttu-id="763b5-120">OS</span><span class="sxs-lookup"><span data-stu-id="763b5-120">PARAMETERS</span></span>

### <span data-ttu-id="763b5-121">-DeleteVHD</span><span class="sxs-lookup"><span data-stu-id="763b5-121">-DeleteVHD</span></span>
<span data-ttu-id="763b5-122">Indica que esse cmdlet Remove o disco de dados e o disco rígido virtual (VHD) do armazenamento BLOB.</span><span class="sxs-lookup"><span data-stu-id="763b5-122">Indicates that this cmdlet removes the data disk and the virtual hard disk (VHD) from blob storage.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="763b5-123">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="763b5-123">-InformationAction</span></span>
<span data-ttu-id="763b5-124">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="763b5-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="763b5-125">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="763b5-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="763b5-126">Contínuo</span><span class="sxs-lookup"><span data-stu-id="763b5-126">Continue</span></span>
- <span data-ttu-id="763b5-127">Ignorar</span><span class="sxs-lookup"><span data-stu-id="763b5-127">Ignore</span></span>
- <span data-ttu-id="763b5-128">Inquire</span><span class="sxs-lookup"><span data-stu-id="763b5-128">Inquire</span></span>
- <span data-ttu-id="763b5-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="763b5-129">SilentlyContinue</span></span>
- <span data-ttu-id="763b5-130">Finaliza</span><span class="sxs-lookup"><span data-stu-id="763b5-130">Stop</span></span>
- <span data-ttu-id="763b5-131">Suspensão</span><span class="sxs-lookup"><span data-stu-id="763b5-131">Suspend</span></span>

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

### <span data-ttu-id="763b5-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="763b5-132">-InformationVariable</span></span>
<span data-ttu-id="763b5-133">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="763b5-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="763b5-134">-LUN</span><span class="sxs-lookup"><span data-stu-id="763b5-134">-LUN</span></span>
<span data-ttu-id="763b5-135">Especifica o número de unidade lógica (LUN) para a unidade de dados na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="763b5-135">Specifies the logical unit number (LUN) for the data drive in the virtual machine.</span></span>
<span data-ttu-id="763b5-136">Os valores válidos são: de 0 a 15.</span><span class="sxs-lookup"><span data-stu-id="763b5-136">Valid values are: 0 through 15.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="763b5-137">-Perfil</span><span class="sxs-lookup"><span data-stu-id="763b5-137">-Profile</span></span>
<span data-ttu-id="763b5-138">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="763b5-138">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="763b5-139">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="763b5-139">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="763b5-140">-VM</span><span class="sxs-lookup"><span data-stu-id="763b5-140">-VM</span></span>
<span data-ttu-id="763b5-141">Especifica o objeto da máquina virtual que está anexado ao disco de dados.</span><span class="sxs-lookup"><span data-stu-id="763b5-141">Specifies the virtual machine object that is attached to the data disk.</span></span>
<span data-ttu-id="763b5-142">Para obter um objeto de máquina virtual, use o cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="763b5-142">To obtain a virtual machine object, use the **Get-AzureVM** cmdlet.</span></span>

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

### <span data-ttu-id="763b5-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="763b5-143">CommonParameters</span></span>
<span data-ttu-id="763b5-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="763b5-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="763b5-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="763b5-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="763b5-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="763b5-146">INPUTS</span></span>

## <span data-ttu-id="763b5-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="763b5-147">OUTPUTS</span></span>

## <span data-ttu-id="763b5-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="763b5-148">NOTES</span></span>

## <span data-ttu-id="763b5-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="763b5-149">RELATED LINKS</span></span>

[<span data-ttu-id="763b5-150">Add-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="763b5-150">Add-AzureDataDisk</span></span>](./Add-AzureDataDisk.md)

[<span data-ttu-id="763b5-151">Get-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="763b5-151">Get-AzureDataDisk</span></span>](./Get-AzureDataDisk.md)

[<span data-ttu-id="763b5-152">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="763b5-152">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="763b5-153">Set-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="763b5-153">Set-AzureDataDisk</span></span>](./Set-AzureDataDisk.md)

[<span data-ttu-id="763b5-154">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="763b5-154">Update-AzureVM</span></span>](./Update-AzureVM.md)


