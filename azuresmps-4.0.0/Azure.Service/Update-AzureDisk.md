---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 849714BC-8B19-453E-B790-A9C38F9D48CB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8ef8bd3b1fef6a3af01193a104f6917c4131064f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945425"
---
# <span data-ttu-id="471ec-101">Update-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="471ec-101">Update-AzureDisk</span></span>

## <span data-ttu-id="471ec-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="471ec-102">SYNOPSIS</span></span>
<span data-ttu-id="471ec-103">Altera o rótulo de um disco no repositório de discos do Azure.</span><span class="sxs-lookup"><span data-stu-id="471ec-103">Changes the label of a disk in the Azure disk repository.</span></span>

## <span data-ttu-id="471ec-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="471ec-104">SYNTAX</span></span>

### <span data-ttu-id="471ec-105">Dimensiona</span><span class="sxs-lookup"><span data-stu-id="471ec-105">Resize</span></span>
```
Update-AzureDisk [-DiskName] <String> [[-Label] <String>] [-ResizedSizeInGB] <Int32>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="471ec-106">NoResize</span><span class="sxs-lookup"><span data-stu-id="471ec-106">NoResize</span></span>
```
Update-AzureDisk [-DiskName] <String> [-Label] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="471ec-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="471ec-107">DESCRIPTION</span></span>
<span data-ttu-id="471ec-108">O cmdlet **Update-AzureDisk** altera o rótulo associado a um disco no repositório de disco da assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="471ec-108">The **Update-AzureDisk** cmdlet changes the label that is associated with a disk in the disk repository of the current Azure subscription.</span></span>

## <span data-ttu-id="471ec-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="471ec-109">EXAMPLES</span></span>

### <span data-ttu-id="471ec-110">Exemplo 1: alterar o rótulo de um disco</span><span class="sxs-lookup"><span data-stu-id="471ec-110">Example 1: Change the label of a disk</span></span>
```
PS C:\> Update-AzureDisk ?DiskName "ContosoOSDisk" -Label "DoNotUse"
```

<span data-ttu-id="471ec-111">Esse comando altera o rótulo do disco chamado ContosoOSDisk para DoNotUse.</span><span class="sxs-lookup"><span data-stu-id="471ec-111">This command changes the label of the disk named ContosoOSDisk to DoNotUse.</span></span>

## <span data-ttu-id="471ec-112">OS</span><span class="sxs-lookup"><span data-stu-id="471ec-112">PARAMETERS</span></span>

### <span data-ttu-id="471ec-113">-Diskname</span><span class="sxs-lookup"><span data-stu-id="471ec-113">-DiskName</span></span>
<span data-ttu-id="471ec-114">Especifica o nome do disco que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="471ec-114">Specifies the name of the disk that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="471ec-115">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="471ec-115">-InformationAction</span></span>
<span data-ttu-id="471ec-116">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="471ec-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="471ec-117">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="471ec-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="471ec-118">Contínuo</span><span class="sxs-lookup"><span data-stu-id="471ec-118">Continue</span></span>
- <span data-ttu-id="471ec-119">Ignorar</span><span class="sxs-lookup"><span data-stu-id="471ec-119">Ignore</span></span>
- <span data-ttu-id="471ec-120">Inquire</span><span class="sxs-lookup"><span data-stu-id="471ec-120">Inquire</span></span>
- <span data-ttu-id="471ec-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="471ec-121">SilentlyContinue</span></span>
- <span data-ttu-id="471ec-122">Finaliza</span><span class="sxs-lookup"><span data-stu-id="471ec-122">Stop</span></span>
- <span data-ttu-id="471ec-123">Suspensão</span><span class="sxs-lookup"><span data-stu-id="471ec-123">Suspend</span></span>

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

### <span data-ttu-id="471ec-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="471ec-124">-InformationVariable</span></span>
<span data-ttu-id="471ec-125">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="471ec-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="471ec-126">-Rótulo</span><span class="sxs-lookup"><span data-stu-id="471ec-126">-Label</span></span>
<span data-ttu-id="471ec-127">Especifica o novo rótulo para o disco.</span><span class="sxs-lookup"><span data-stu-id="471ec-127">Specifies the new label for the disk.</span></span>

```yaml
Type: String
Parameter Sets: Resize
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: NoResize
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="471ec-128">-Perfil</span><span class="sxs-lookup"><span data-stu-id="471ec-128">-Profile</span></span>
<span data-ttu-id="471ec-129">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="471ec-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="471ec-130">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="471ec-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="471ec-131">-ResizedSizeInGB</span><span class="sxs-lookup"><span data-stu-id="471ec-131">-ResizedSizeInGB</span></span>
<span data-ttu-id="471ec-132">Especifica o novo tamanho, em gigabytes, para o disco.</span><span class="sxs-lookup"><span data-stu-id="471ec-132">Specifies the new size, in gigabytes, for the disk.</span></span>

```yaml
Type: Int32
Parameter Sets: Resize
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="471ec-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="471ec-133">CommonParameters</span></span>
<span data-ttu-id="471ec-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="471ec-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="471ec-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="471ec-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="471ec-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="471ec-136">INPUTS</span></span>

## <span data-ttu-id="471ec-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="471ec-137">OUTPUTS</span></span>

### <span data-ttu-id="471ec-138">DiskContext</span><span class="sxs-lookup"><span data-stu-id="471ec-138">DiskContext</span></span>

## <span data-ttu-id="471ec-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="471ec-139">NOTES</span></span>

## <span data-ttu-id="471ec-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="471ec-140">RELATED LINKS</span></span>

[<span data-ttu-id="471ec-141">Add-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="471ec-141">Add-AzureDisk</span></span>](./Add-AzureDisk.md)

[<span data-ttu-id="471ec-142">Get-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="471ec-142">Get-AzureDisk</span></span>](./Get-AzureDisk.md)

[<span data-ttu-id="471ec-143">Remove-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="471ec-143">Remove-AzureDisk</span></span>](./Remove-AzureDisk.md)


