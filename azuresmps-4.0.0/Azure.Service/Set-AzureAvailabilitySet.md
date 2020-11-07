---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: E0590AD4-F67B-48EF-8657-8890A2204CB6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 607cd288bcc9c86209a3ae0af569e964205f5cb4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946067"
---
# <span data-ttu-id="75c40-101">Set-AzureAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="75c40-101">Set-AzureAvailabilitySet</span></span>

## <span data-ttu-id="75c40-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="75c40-102">SYNOPSIS</span></span>
<span data-ttu-id="75c40-103">Define o nome da disponibilidade definida em uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="75c40-103">Sets the name of the availability set on an Azure virtual machine.</span></span>

## <span data-ttu-id="75c40-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="75c40-104">SYNTAX</span></span>

```
Set-AzureAvailabilitySet [-AvailabilitySetName] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="75c40-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="75c40-105">DESCRIPTION</span></span>
<span data-ttu-id="75c40-106">O cmdlet **set-AzureAvailabilitySet** define o nome do conjunto de disponibilidade em uma máquina virtual do Azure após a implantação.</span><span class="sxs-lookup"><span data-stu-id="75c40-106">The **Set-AzureAvailabilitySet** cmdlet sets the name of the availability set on an Azure virtual machine after deployment.</span></span>

## <span data-ttu-id="75c40-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="75c40-107">EXAMPLES</span></span>

### <span data-ttu-id="75c40-108">Exemplo 1: modificar o nome de um conjunto de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="75c40-108">Example 1: Modify the name of an availability set</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine24" | Set-AzureAvailabilitySet -AvailabilitySetName "AvailabilitySet14" | Update-AzureVM
```

<span data-ttu-id="75c40-109">O primeiro comando obtém a máquina virtual chamada VirtualMachine07 no serviço chamado ContosoService usando o cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="75c40-109">The first command gets the virtual machine named VirtualMachine07 in the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="75c40-110">O comando passa o objeto para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="75c40-110">The command passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="75c40-111">Esse cmdlet modifica o nome do conjunto de disponibilidade para essa máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="75c40-111">That cmdlet modifies the name of the availability set for that virtual machine.</span></span>
<span data-ttu-id="75c40-112">O comando atualiza a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="75c40-112">The command updates the virtual machine.</span></span>

## <span data-ttu-id="75c40-113">OS</span><span class="sxs-lookup"><span data-stu-id="75c40-113">PARAMETERS</span></span>

### <span data-ttu-id="75c40-114">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="75c40-114">-AvailabilitySetName</span></span>
<span data-ttu-id="75c40-115">Especifica o nome do conjunto de disponibilidade ao qual a máquina virtual pertence.</span><span class="sxs-lookup"><span data-stu-id="75c40-115">Specifies the name of the availability set to which the virtual machine belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75c40-116">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="75c40-116">-InformationAction</span></span>
<span data-ttu-id="75c40-117">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="75c40-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="75c40-118">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="75c40-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="75c40-119">Contínuo</span><span class="sxs-lookup"><span data-stu-id="75c40-119">Continue</span></span>
- <span data-ttu-id="75c40-120">Ignorar</span><span class="sxs-lookup"><span data-stu-id="75c40-120">Ignore</span></span>
- <span data-ttu-id="75c40-121">Inquire</span><span class="sxs-lookup"><span data-stu-id="75c40-121">Inquire</span></span>
- <span data-ttu-id="75c40-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="75c40-122">SilentlyContinue</span></span>
- <span data-ttu-id="75c40-123">Finaliza</span><span class="sxs-lookup"><span data-stu-id="75c40-123">Stop</span></span>
- <span data-ttu-id="75c40-124">Suspensão</span><span class="sxs-lookup"><span data-stu-id="75c40-124">Suspend</span></span>

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

### <span data-ttu-id="75c40-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="75c40-125">-InformationVariable</span></span>
<span data-ttu-id="75c40-126">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="75c40-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="75c40-127">-Perfil</span><span class="sxs-lookup"><span data-stu-id="75c40-127">-Profile</span></span>
<span data-ttu-id="75c40-128">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="75c40-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="75c40-129">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="75c40-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="75c40-130">-VM</span><span class="sxs-lookup"><span data-stu-id="75c40-130">-VM</span></span>
<span data-ttu-id="75c40-131">Especifica a configuração de máquina virtual que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="75c40-131">Specifies the virtual machine configuration that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="75c40-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75c40-132">CommonParameters</span></span>
<span data-ttu-id="75c40-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75c40-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75c40-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75c40-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75c40-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="75c40-135">INPUTS</span></span>

## <span data-ttu-id="75c40-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="75c40-136">OUTPUTS</span></span>

## <span data-ttu-id="75c40-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="75c40-137">NOTES</span></span>

## <span data-ttu-id="75c40-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="75c40-138">RELATED LINKS</span></span>

[<span data-ttu-id="75c40-139">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="75c40-139">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="75c40-140">Remove-AzureAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="75c40-140">Remove-AzureAvailabilitySet</span></span>](./Remove-AzureAvailabilitySet.md)


