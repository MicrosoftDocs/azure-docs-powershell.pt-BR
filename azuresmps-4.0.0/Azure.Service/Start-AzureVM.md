---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: C60F78AE-3803-4D9F-A4F3-EAA42052C0E4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6a0708ca37cdb2b700772da2fe9cb684b8b29a30
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945771"
---
# <span data-ttu-id="7cc36-101">Start-AzureVM</span><span class="sxs-lookup"><span data-stu-id="7cc36-101">Start-AzureVM</span></span>

## <span data-ttu-id="7cc36-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7cc36-102">SYNOPSIS</span></span>
<span data-ttu-id="7cc36-103">Inicia uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="7cc36-103">Starts an Azure virtual machine.</span></span>

## <span data-ttu-id="7cc36-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7cc36-104">SYNTAX</span></span>

### <span data-ttu-id="7cc36-105">ByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="7cc36-105">ByName (Default)</span></span>
```
Start-AzureVM [-Name] <String[]> [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="7cc36-106">Contribuição</span><span class="sxs-lookup"><span data-stu-id="7cc36-106">Input</span></span>
```
Start-AzureVM -VM <IPersistentVM[]> [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="7cc36-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7cc36-107">DESCRIPTION</span></span>
<span data-ttu-id="7cc36-108">O cmdlet **Start-AzureVM** solicita o início de uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="7cc36-108">The **Start-AzureVM** cmdlet requests the start of an Azure virtual machine.</span></span>

## <span data-ttu-id="7cc36-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7cc36-109">EXAMPLES</span></span>

### <span data-ttu-id="7cc36-110">Exemplo 1: iniciar uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="7cc36-110">Example 1: Start a virtual machine</span></span>
```
PS C:\> Start-AzureVM -ServiceName "ContosoService03" -Name "VirtualMachine04"
```

<span data-ttu-id="7cc36-111">Esse comando inicia a máquina virtual chamada VirtualMachine04 que é executada no serviço do Azure chamado ContosoService03.</span><span class="sxs-lookup"><span data-stu-id="7cc36-111">This command starts the virtual machine named VirtualMachine04 that runs in the Azure service named ContosoService03.</span></span>

### <span data-ttu-id="7cc36-112">Exemplo 2: iniciar uma máquina virtual usando um objeto de máquina virtual</span><span class="sxs-lookup"><span data-stu-id="7cc36-112">Example 2: Start a virtual machine by using a virtual machine object</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService03" -Name "DatabaseServer" | Start-AzureVM
```

<span data-ttu-id="7cc36-113">Esse comando recupera o objeto da máquina virtual para a máquina virtual cujo nome é servidor e, em seguida, pede para iniciá-lo.</span><span class="sxs-lookup"><span data-stu-id="7cc36-113">This command retrieves the virtual machine object for the virtual machine whose name is DatabaseServer, and then requests to start it.</span></span>

## <span data-ttu-id="7cc36-114">OS</span><span class="sxs-lookup"><span data-stu-id="7cc36-114">PARAMETERS</span></span>

### <span data-ttu-id="7cc36-115">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="7cc36-115">-InformationAction</span></span>
<span data-ttu-id="7cc36-116">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="7cc36-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="7cc36-117">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="7cc36-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7cc36-118">Contínuo</span><span class="sxs-lookup"><span data-stu-id="7cc36-118">Continue</span></span>
- <span data-ttu-id="7cc36-119">Ignorar</span><span class="sxs-lookup"><span data-stu-id="7cc36-119">Ignore</span></span>
- <span data-ttu-id="7cc36-120">Inquire</span><span class="sxs-lookup"><span data-stu-id="7cc36-120">Inquire</span></span>
- <span data-ttu-id="7cc36-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="7cc36-121">SilentlyContinue</span></span>
- <span data-ttu-id="7cc36-122">Finaliza</span><span class="sxs-lookup"><span data-stu-id="7cc36-122">Stop</span></span>
- <span data-ttu-id="7cc36-123">Suspensão</span><span class="sxs-lookup"><span data-stu-id="7cc36-123">Suspend</span></span>

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

### <span data-ttu-id="7cc36-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="7cc36-124">-InformationVariable</span></span>
<span data-ttu-id="7cc36-125">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="7cc36-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="7cc36-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="7cc36-126">-Name</span></span>
<span data-ttu-id="7cc36-127">Especifica o nome da máquina virtual a ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="7cc36-127">Specifies the name of the virtual machine to start.</span></span>

```yaml
Type: String[]
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cc36-128">-Perfil</span><span class="sxs-lookup"><span data-stu-id="7cc36-128">-Profile</span></span>
<span data-ttu-id="7cc36-129">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="7cc36-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7cc36-130">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="7cc36-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7cc36-131">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="7cc36-131">-ServiceName</span></span>
<span data-ttu-id="7cc36-132">Especifica o nome do serviço do Azure que contém a máquina virtual a ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="7cc36-132">Specifies the name of the Azure service that contains the virtual machine to start.</span></span>

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

### <span data-ttu-id="7cc36-133">-VM</span><span class="sxs-lookup"><span data-stu-id="7cc36-133">-VM</span></span>
<span data-ttu-id="7cc36-134">Especifica um objeto de máquina virtual que identifica a máquina virtual para iniciar.</span><span class="sxs-lookup"><span data-stu-id="7cc36-134">Specifies a virtual machine object that identifies the virtual machine to start.</span></span>

```yaml
Type: IPersistentVM[]
Parameter Sets: Input
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cc36-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cc36-135">CommonParameters</span></span>
<span data-ttu-id="7cc36-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7cc36-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cc36-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7cc36-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cc36-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7cc36-138">INPUTS</span></span>

## <span data-ttu-id="7cc36-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7cc36-139">OUTPUTS</span></span>

## <span data-ttu-id="7cc36-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7cc36-140">NOTES</span></span>

## <span data-ttu-id="7cc36-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7cc36-141">RELATED LINKS</span></span>

[<span data-ttu-id="7cc36-142">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="7cc36-142">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="7cc36-143">Remove-AzureVM</span><span class="sxs-lookup"><span data-stu-id="7cc36-143">Remove-AzureVM</span></span>](./Remove-AzureVM.md)

[<span data-ttu-id="7cc36-144">Restart-AzureVM</span><span class="sxs-lookup"><span data-stu-id="7cc36-144">Restart-AzureVM</span></span>](./Restart-AzureVM.md)

[<span data-ttu-id="7cc36-145">Parar-AzureVM</span><span class="sxs-lookup"><span data-stu-id="7cc36-145">Stop-AzureVM</span></span>](./Stop-AzureVM.md)

[<span data-ttu-id="7cc36-146">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="7cc36-146">Update-AzureVM</span></span>](./Update-AzureVM.md)


