---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 75A50C59-28D1-4D29-A420-D24BF479F79E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 29e5e7e0bc2fcc0ce93186cf966f18d6c9c3e372
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946157"
---
# <span data-ttu-id="14da4-101">Remove-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="14da4-101">Remove-AzureDisk</span></span>

## <span data-ttu-id="14da4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="14da4-102">SYNOPSIS</span></span>
<span data-ttu-id="14da4-103">Remove um disco do repositório de discos do Azure.</span><span class="sxs-lookup"><span data-stu-id="14da4-103">Removes a disk from the Azure disk repository.</span></span>

## <span data-ttu-id="14da4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="14da4-104">SYNTAX</span></span>

```
Remove-AzureDisk [-DiskName] <String> [-DeleteVHD] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="14da4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="14da4-105">DESCRIPTION</span></span>
<span data-ttu-id="14da4-106">O cmdlet **Remove-AzureDisk** remove um disco do repositório do Azure Disk na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="14da4-106">The **Remove-AzureDisk** cmdlet removes a disk from the Azure disk repository in the current subscription.</span></span>
<span data-ttu-id="14da4-107">Por padrão, esse cmdlet não exclui o arquivo de disco rígido virtual (VHD) do armazenamento BLOB.</span><span class="sxs-lookup"><span data-stu-id="14da4-107">By default, this cmdlet does not delete the virtual hard disk (VHD) file from blob storage.</span></span>
<span data-ttu-id="14da4-108">Para excluir o VHD, especifique o parâmetro *DeleteVHD* .</span><span class="sxs-lookup"><span data-stu-id="14da4-108">To delete the VHD, specify the *DeleteVHD* parameter.</span></span>

## <span data-ttu-id="14da4-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="14da4-109">EXAMPLES</span></span>

### <span data-ttu-id="14da4-110">Exemplo 1: remover um disco</span><span class="sxs-lookup"><span data-stu-id="14da4-110">Example 1: Remove a disk</span></span>
```
PS C:\> Remove-AzureDisk -DiskName "ContosoDataDisk"
```

<span data-ttu-id="14da4-111">Esse comando Remove o disco denominado ContosoDataDisk Disk do repositório de discos.</span><span class="sxs-lookup"><span data-stu-id="14da4-111">This command removes the disk named ContosoDataDisk disk from the disk repository.</span></span>
<span data-ttu-id="14da4-112">O comando não exclui o VHD.</span><span class="sxs-lookup"><span data-stu-id="14da4-112">The command does not delete the VHD.</span></span>

### <span data-ttu-id="14da4-113">Exemplo 2: remover e excluir um disco</span><span class="sxs-lookup"><span data-stu-id="14da4-113">Example 2: Remove and delete a disk</span></span>
```
PS C:\> Remove-AzureDisk -DiskName "ContosoDataDisk" -DeleteVHD
```

<span data-ttu-id="14da4-114">Esse comando Remove o disco denominado ContosoDataDisk Disk do repositório de discos.</span><span class="sxs-lookup"><span data-stu-id="14da4-114">This command removes the disk named ContosoDataDisk disk from the disk repository.</span></span>
<span data-ttu-id="14da4-115">Esse comando especifica o parâmetro DeleteVHD.</span><span class="sxs-lookup"><span data-stu-id="14da4-115">This command specifies the DeleteVHD parameter.</span></span>
<span data-ttu-id="14da4-116">Portanto, o comando exclui o VHD do armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="14da4-116">Therefore, the command deletes the VHD from Azure Storage.</span></span>

## <span data-ttu-id="14da4-117">OS</span><span class="sxs-lookup"><span data-stu-id="14da4-117">PARAMETERS</span></span>

### <span data-ttu-id="14da4-118">-DeleteVHD</span><span class="sxs-lookup"><span data-stu-id="14da4-118">-DeleteVHD</span></span>
<span data-ttu-id="14da4-119">Indica que esse cmdlet Remove o VHD do armazenamento de BLOB.</span><span class="sxs-lookup"><span data-stu-id="14da4-119">Indicates that this cmdlet removes the VHD from blob storage.</span></span>

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

### <span data-ttu-id="14da4-120">-Diskname</span><span class="sxs-lookup"><span data-stu-id="14da4-120">-DiskName</span></span>
<span data-ttu-id="14da4-121">Especifica o nome do disco de dados no repositório de discos que esse cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="14da4-121">Specifies the name of the data disk in the disk repository that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14da4-122">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="14da4-122">-InformationAction</span></span>
<span data-ttu-id="14da4-123">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="14da4-123">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="14da4-124">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="14da4-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="14da4-125">Contínuo</span><span class="sxs-lookup"><span data-stu-id="14da4-125">Continue</span></span>
- <span data-ttu-id="14da4-126">Ignorar</span><span class="sxs-lookup"><span data-stu-id="14da4-126">Ignore</span></span>
- <span data-ttu-id="14da4-127">Inquire</span><span class="sxs-lookup"><span data-stu-id="14da4-127">Inquire</span></span>
- <span data-ttu-id="14da4-128">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="14da4-128">SilentlyContinue</span></span>
- <span data-ttu-id="14da4-129">Finaliza</span><span class="sxs-lookup"><span data-stu-id="14da4-129">Stop</span></span>
- <span data-ttu-id="14da4-130">Suspensão</span><span class="sxs-lookup"><span data-stu-id="14da4-130">Suspend</span></span>

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

### <span data-ttu-id="14da4-131">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="14da4-131">-InformationVariable</span></span>
<span data-ttu-id="14da4-132">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="14da4-132">Specifies an information variable.</span></span>

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

### <span data-ttu-id="14da4-133">-Perfil</span><span class="sxs-lookup"><span data-stu-id="14da4-133">-Profile</span></span>
<span data-ttu-id="14da4-134">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="14da4-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="14da4-135">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="14da4-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="14da4-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14da4-136">CommonParameters</span></span>
<span data-ttu-id="14da4-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14da4-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14da4-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14da4-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14da4-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="14da4-139">INPUTS</span></span>

## <span data-ttu-id="14da4-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="14da4-140">OUTPUTS</span></span>

## <span data-ttu-id="14da4-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="14da4-141">NOTES</span></span>

## <span data-ttu-id="14da4-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="14da4-142">RELATED LINKS</span></span>

[<span data-ttu-id="14da4-143">Add-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="14da4-143">Add-AzureDisk</span></span>](./Add-AzureDisk.md)

[<span data-ttu-id="14da4-144">Get-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="14da4-144">Get-AzureDisk</span></span>](./Get-AzureDisk.md)

[<span data-ttu-id="14da4-145">Update-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="14da4-145">Update-AzureDisk</span></span>](./Update-AzureDisk.md)


