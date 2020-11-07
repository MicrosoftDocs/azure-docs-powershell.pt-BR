---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 95DCD2EC-8327-4A46-B624-289D0A28F7EA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4614910b8c0ccd36bb8ef75ee98f662cf69a276a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946354"
---
# <span data-ttu-id="a209e-101">Get-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="a209e-101">Get-AzureDisk</span></span>

## <span data-ttu-id="a209e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a209e-102">SYNOPSIS</span></span>
<span data-ttu-id="a209e-103">Obtém informações sobre discos no repositório de discos do Azure.</span><span class="sxs-lookup"><span data-stu-id="a209e-103">Gets information about disks in the Azure disk repository.</span></span>

## <span data-ttu-id="a209e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a209e-104">SYNTAX</span></span>

```
Get-AzureDisk [[-DiskName] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="a209e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a209e-105">DESCRIPTION</span></span>
<span data-ttu-id="a209e-106">O cmdlet **Get-AzureDisk** Obtém informações sobre os discos que são armazenados no repositório de discos do Azure para a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="a209e-106">The **Get-AzureDisk** cmdlet gets information about the disks that are stored in the Azure disk repository for the current subscription.</span></span>
<span data-ttu-id="a209e-107">Esse cmdlet retorna uma lista de informações para todos os discos no repositório.</span><span class="sxs-lookup"><span data-stu-id="a209e-107">This cmdlet returns a list of information for all disks in the repository.</span></span>
<span data-ttu-id="a209e-108">Para ver as informações de um disco específico, especifique o nome do disco.</span><span class="sxs-lookup"><span data-stu-id="a209e-108">To view information for a specific disk, specify the name of the disk.</span></span>

## <span data-ttu-id="a209e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a209e-109">EXAMPLES</span></span>

### <span data-ttu-id="a209e-110">Exemplo 1: obter informações sobre um disco</span><span class="sxs-lookup"><span data-stu-id="a209e-110">Example 1: Get information about a disk</span></span>
```
PS C:\> Get-AzureDisk -DiskName "ContosoDataDisk"
```

<span data-ttu-id="a209e-111">Este comando obtém dados de informações sobre o disco chamado ContosoDataDisk do repositório de discos.</span><span class="sxs-lookup"><span data-stu-id="a209e-111">This command gets information data about the disk named ContosoDataDisk from the disk repository.</span></span>

### <span data-ttu-id="a209e-112">Exemplo 2: obter informações sobre todos os discos</span><span class="sxs-lookup"><span data-stu-id="a209e-112">Example 2: Get information about all disks</span></span>
```
PS C:\> Get-AzureDisk
```

<span data-ttu-id="a209e-113">Esse comando obtém informações sobre todos os discos no repositório de discos.</span><span class="sxs-lookup"><span data-stu-id="a209e-113">This command gets information about all the disks in the disk repository.</span></span>

### <span data-ttu-id="a209e-114">Exemplo 3: obter informações sobre um disco</span><span class="sxs-lookup"><span data-stu-id="a209e-114">Example 3: Get information about a disk</span></span>
```
PS C:\> Get-AzureDisk | Where-Object {$_.AttachedTo -eq $Null } | Format-Table -AutoSize -Property "DiskName","DiskSizeInGB","MediaLink"
```

<span data-ttu-id="a209e-115">Esse comando obtém dados de todos os discos no repositório de disco que não estão atualmente conectados a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a209e-115">This command gets data for all of the disks in the disk repository that are not currently attached to a virtual machine.</span></span>
<span data-ttu-id="a209e-116">O comando obtém informações sobre todos os discos e passa cada objeto para o cmdlet **Where-Object** .</span><span class="sxs-lookup"><span data-stu-id="a209e-116">The command gets information about all of the disks, and passes each object to the **Where-Object** cmdlet.</span></span>
<span data-ttu-id="a209e-117">Esse cmdlet descartará qualquer disco que não tenha um valor de $Null para a propriedade **Attachedto** .</span><span class="sxs-lookup"><span data-stu-id="a209e-117">That cmdlet drops any disk that does not have a value of $Null for the **AttachedTo** property.</span></span>
<span data-ttu-id="a209e-118">O comando formata a lista como uma tabela usando o cmdlet **Format-Table** .</span><span class="sxs-lookup"><span data-stu-id="a209e-118">The command formats the list as a table by using the **Format-Table** cmdlet.</span></span>

## <span data-ttu-id="a209e-119">OS</span><span class="sxs-lookup"><span data-stu-id="a209e-119">PARAMETERS</span></span>

### <span data-ttu-id="a209e-120">-Diskname</span><span class="sxs-lookup"><span data-stu-id="a209e-120">-DiskName</span></span>
<span data-ttu-id="a209e-121">Especifica o nome do disco no repositório de disco sobre o qual esse cmdlet obtém informações.</span><span class="sxs-lookup"><span data-stu-id="a209e-121">Specifies the name of the disk in the disk repository about which this cmdlet gets information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a209e-122">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="a209e-122">-InformationAction</span></span>
<span data-ttu-id="a209e-123">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="a209e-123">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="a209e-124">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="a209e-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a209e-125">Contínuo</span><span class="sxs-lookup"><span data-stu-id="a209e-125">Continue</span></span>
- <span data-ttu-id="a209e-126">Ignorar</span><span class="sxs-lookup"><span data-stu-id="a209e-126">Ignore</span></span>
- <span data-ttu-id="a209e-127">Inquire</span><span class="sxs-lookup"><span data-stu-id="a209e-127">Inquire</span></span>
- <span data-ttu-id="a209e-128">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a209e-128">SilentlyContinue</span></span>
- <span data-ttu-id="a209e-129">Finaliza</span><span class="sxs-lookup"><span data-stu-id="a209e-129">Stop</span></span>
- <span data-ttu-id="a209e-130">Suspensão</span><span class="sxs-lookup"><span data-stu-id="a209e-130">Suspend</span></span>

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

### <span data-ttu-id="a209e-131">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a209e-131">-InformationVariable</span></span>
<span data-ttu-id="a209e-132">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="a209e-132">Specifies an information variable.</span></span>

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

### <span data-ttu-id="a209e-133">-Perfil</span><span class="sxs-lookup"><span data-stu-id="a209e-133">-Profile</span></span>
<span data-ttu-id="a209e-134">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="a209e-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a209e-135">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="a209e-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a209e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a209e-136">CommonParameters</span></span>
<span data-ttu-id="a209e-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a209e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a209e-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a209e-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a209e-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a209e-139">INPUTS</span></span>

## <span data-ttu-id="a209e-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a209e-140">OUTPUTS</span></span>

## <span data-ttu-id="a209e-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a209e-141">NOTES</span></span>

## <span data-ttu-id="a209e-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a209e-142">RELATED LINKS</span></span>

[<span data-ttu-id="a209e-143">Add-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="a209e-143">Add-AzureDisk</span></span>](./Add-AzureDisk.md)

[<span data-ttu-id="a209e-144">Remove-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="a209e-144">Remove-AzureDisk</span></span>](./Remove-AzureDisk.md)

[<span data-ttu-id="a209e-145">Update-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="a209e-145">Update-AzureDisk</span></span>](./Update-AzureDisk.md)


