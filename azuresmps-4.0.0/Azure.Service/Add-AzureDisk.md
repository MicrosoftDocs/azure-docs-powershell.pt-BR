---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 16A34F31-1C61-4911-8C1F-9F82683524A1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 775d2deff8a83e758d48fb9328bf4156b142d20c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946393"
---
# <span data-ttu-id="63219-101">Add-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="63219-101">Add-AzureDisk</span></span>

## <span data-ttu-id="63219-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="63219-102">SYNOPSIS</span></span>
<span data-ttu-id="63219-103">Adiciona um disco ao repositório de discos do Azure.</span><span class="sxs-lookup"><span data-stu-id="63219-103">Adds a disk to the Azure disk repository.</span></span>

## <span data-ttu-id="63219-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="63219-104">SYNTAX</span></span>

```
Add-AzureDisk [-DiskName] <String> [-MediaLocation] <String> [-Label <String>] [-OS <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="63219-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="63219-105">DESCRIPTION</span></span>
<span data-ttu-id="63219-106">O cmdlet **Add-AzureDisk** adiciona um disco ao repositório de disco do Azure na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="63219-106">The **Add-AzureDisk** cmdlet adds a disk to the Azure disk repository in the current subscription.</span></span>
<span data-ttu-id="63219-107">Esse cmdlet pode adicionar um disco de sistema ou um disco de dados.</span><span class="sxs-lookup"><span data-stu-id="63219-107">This cmdlet can add a system disk or a data disk.</span></span>
<span data-ttu-id="63219-108">Para adicionar um disco do sistema, especifique um tipo de sistema operacional usando o parâmetro *sistema* operacional.</span><span class="sxs-lookup"><span data-stu-id="63219-108">To add a system disk, specify an operating system type by using the *OS* parameter.</span></span>

## <span data-ttu-id="63219-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="63219-109">EXAMPLES</span></span>

### <span data-ttu-id="63219-110">Exemplo 1: adicionar um disco de inicialização que use o sistema operacional Windows</span><span class="sxs-lookup"><span data-stu-id="63219-110">Example 1: Add a startup disk that uses the Windows operating system</span></span>
```
PS C:\> Add-AzureDisk -DiskName "MyWinDisk" -MediaLocation "http://contosostorage.blob.core.azure.com/vhds/winserver-system.vhd" -Label "StartupDisk" -OS "Windows"
```

<span data-ttu-id="63219-111">Esse comando adiciona um disco de sistema ao repositório de disco.</span><span class="sxs-lookup"><span data-stu-id="63219-111">This command adds a system disk to your disk repository.</span></span>
<span data-ttu-id="63219-112">O disco do sistema usa o sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="63219-112">The system disk uses the Windows operating system.</span></span>

### <span data-ttu-id="63219-113">Exemplo 2: adicionar um disco de dados</span><span class="sxs-lookup"><span data-stu-id="63219-113">Example 2: Add a data disk</span></span>
```
PS C:\> Add-AzureDisk -DiskName "MyDataDisk" -MediaLocation "http://yourstorageaccount.blob.core.azure.com/vhds/winserver-data.vhd" -Label "DataDisk"
```

<span data-ttu-id="63219-114">Esse comando adiciona um disco de dados.</span><span class="sxs-lookup"><span data-stu-id="63219-114">This command adds a data disk.</span></span>

### <span data-ttu-id="63219-115">Exemplo 3: adicionar um disco de sistema Linux</span><span class="sxs-lookup"><span data-stu-id="63219-115">Example 3: Add a Linux system disk</span></span>
```
PS C:\> Add-AzureDisk -DiskName "MyLinuxDisk" -MediaLocation "http://yourstorageaccount.blob.core.azure.com/vhds/linuxsys.vhd" -OS "Linux"
```

<span data-ttu-id="63219-116">Esse comando adiciona um disco do sistema Linux.</span><span class="sxs-lookup"><span data-stu-id="63219-116">This command adds a Linux system disk.</span></span>

## <span data-ttu-id="63219-117">OS</span><span class="sxs-lookup"><span data-stu-id="63219-117">PARAMETERS</span></span>

### <span data-ttu-id="63219-118">-Diskname</span><span class="sxs-lookup"><span data-stu-id="63219-118">-DiskName</span></span>
<span data-ttu-id="63219-119">Especifica o nome do disco que este cmdlet adiciona.</span><span class="sxs-lookup"><span data-stu-id="63219-119">Specifies the name of the disk that this cmdlet adds.</span></span>

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

### <span data-ttu-id="63219-120">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="63219-120">-InformationAction</span></span>
<span data-ttu-id="63219-121">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="63219-121">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="63219-122">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="63219-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="63219-123">Contínuo</span><span class="sxs-lookup"><span data-stu-id="63219-123">Continue</span></span>
- <span data-ttu-id="63219-124">Ignorar</span><span class="sxs-lookup"><span data-stu-id="63219-124">Ignore</span></span>
- <span data-ttu-id="63219-125">Inquire</span><span class="sxs-lookup"><span data-stu-id="63219-125">Inquire</span></span>
- <span data-ttu-id="63219-126">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="63219-126">SilentlyContinue</span></span>
- <span data-ttu-id="63219-127">Finaliza</span><span class="sxs-lookup"><span data-stu-id="63219-127">Stop</span></span>
- <span data-ttu-id="63219-128">Suspensão</span><span class="sxs-lookup"><span data-stu-id="63219-128">Suspend</span></span>

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

### <span data-ttu-id="63219-129">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="63219-129">-InformationVariable</span></span>
<span data-ttu-id="63219-130">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="63219-130">Specifies an information variable.</span></span>

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

### <span data-ttu-id="63219-131">-Rótulo</span><span class="sxs-lookup"><span data-stu-id="63219-131">-Label</span></span>
<span data-ttu-id="63219-132">Especifica um rótulo de disco para o disco que este cmdlet adiciona.</span><span class="sxs-lookup"><span data-stu-id="63219-132">Specifies a disk label for the disk that this cmdlet adds.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63219-133">-MediaLocation</span><span class="sxs-lookup"><span data-stu-id="63219-133">-MediaLocation</span></span>
<span data-ttu-id="63219-134">Especifica o local físico do disco no armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="63219-134">Specifies the physical location of the disk in Azure Storage.</span></span>
<span data-ttu-id="63219-135">Esse valor se refere a uma página blob na conta atual de assinatura e armazenamento.</span><span class="sxs-lookup"><span data-stu-id="63219-135">This value refers to a blob page in the current subscription and storage account.</span></span>

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

### <span data-ttu-id="63219-136">-OS</span><span class="sxs-lookup"><span data-stu-id="63219-136">-OS</span></span>
<span data-ttu-id="63219-137">Especifica o tipo de sistema operacional para um disco de sistema.</span><span class="sxs-lookup"><span data-stu-id="63219-137">Specifies the operating system type for a system disk.</span></span>
<span data-ttu-id="63219-138">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="63219-138">Valid values are:</span></span> 

- <span data-ttu-id="63219-139">Windows</span><span class="sxs-lookup"><span data-stu-id="63219-139">Windows</span></span> 
- <span data-ttu-id="63219-140">Linux</span><span class="sxs-lookup"><span data-stu-id="63219-140">Linux</span></span> 

<span data-ttu-id="63219-141">Se você não especificar esse parâmetro, o cmdlet adicionará o disco como um disco de dados.</span><span class="sxs-lookup"><span data-stu-id="63219-141">If you do not specify this parameter, the cmdlet adds the disk as a data disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63219-142">-Perfil</span><span class="sxs-lookup"><span data-stu-id="63219-142">-Profile</span></span>
<span data-ttu-id="63219-143">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="63219-143">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="63219-144">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="63219-144">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="63219-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63219-145">CommonParameters</span></span>
<span data-ttu-id="63219-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63219-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63219-147">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63219-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63219-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="63219-148">INPUTS</span></span>

## <span data-ttu-id="63219-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="63219-149">OUTPUTS</span></span>

### <span data-ttu-id="63219-150">DiskContext</span><span class="sxs-lookup"><span data-stu-id="63219-150">DiskContext</span></span>

## <span data-ttu-id="63219-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="63219-151">NOTES</span></span>

## <span data-ttu-id="63219-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="63219-152">RELATED LINKS</span></span>

[<span data-ttu-id="63219-153">Get-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="63219-153">Get-AzureDisk</span></span>](./Get-AzureDisk.md)

[<span data-ttu-id="63219-154">Remove-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="63219-154">Remove-AzureDisk</span></span>](./Remove-AzureDisk.md)

[<span data-ttu-id="63219-155">Update-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="63219-155">Update-AzureDisk</span></span>](./Update-AzureDisk.md)


