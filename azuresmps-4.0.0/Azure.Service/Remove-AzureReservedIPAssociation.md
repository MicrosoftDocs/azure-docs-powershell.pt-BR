---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: A6964C80-1991-46FC-84C8-5B00616386BE
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9e43f841fea77626c18edbda541fa011e95faceb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946136"
---
# <span data-ttu-id="de72f-101">Remove-AzureReservedIPAssociation</span><span class="sxs-lookup"><span data-stu-id="de72f-101">Remove-AzureReservedIPAssociation</span></span>

## <span data-ttu-id="de72f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="de72f-102">SYNOPSIS</span></span>
<span data-ttu-id="de72f-103">Remove a associação do endereço IP reservado para a VM ou o serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="de72f-103">Removes the association from the reserved IP address to the VM or cloud service.</span></span>

## <span data-ttu-id="de72f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="de72f-104">SYNTAX</span></span>

```
Remove-AzureReservedIPAssociation [-ReservedIPName] <String> [-ServiceName] <String>
 [[-VirtualIPName] <String>] [[-Slot] <String>] [-Force] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="de72f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="de72f-105">DESCRIPTION</span></span>
<span data-ttu-id="de72f-106">O cmdlet **Remove-AzureReservedIPAssociation** dissocia um endereço IP reservado de uma máquina virtual (VM) ou de um serviço na nuvem.</span><span class="sxs-lookup"><span data-stu-id="de72f-106">The **Remove-AzureReservedIPAssociation** cmdlet disassociates a reserved IP address from a virtual machine (VM) or Cloud Service.</span></span>
<span data-ttu-id="de72f-107">Quando a operação é concluída, o endereço IP reservado é gratuito e a VM/VIP Obtém um endereço IP público dinâmico do inventário do Azure.</span><span class="sxs-lookup"><span data-stu-id="de72f-107">When the operation completes, the reserved IP address is free and the VM/VIP gets a dynamic public IP Address from the Azure Inventory.</span></span>

## <span data-ttu-id="de72f-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="de72f-108">EXAMPLES</span></span>

### <span data-ttu-id="de72f-109">Exemplo 1: remover uma associação de IP reservado</span><span class="sxs-lookup"><span data-stu-id="de72f-109">Example 1: Remove a reserved IP association</span></span>
```
PS C:\> Remove-AzureReservedIPAssociation -ReservedIPName "ResIp14" -ServiceName "PipTestWestEurope"
```

<span data-ttu-id="de72f-110">Esse comando desassocia o endereço IP reservado chamado ResIp14 do serviço chamado PipTestWestEurope.</span><span class="sxs-lookup"><span data-stu-id="de72f-110">This command disassociates the reserved IP address named ResIp14 from the service named PipTestWestEurope.</span></span>
<span data-ttu-id="de72f-111">PipTestWestEurope será atribuído um novo VIP dinâmico.</span><span class="sxs-lookup"><span data-stu-id="de72f-111">PipTestWestEurope will be assigned a new dynamic VIP.</span></span>

## <span data-ttu-id="de72f-112">OS</span><span class="sxs-lookup"><span data-stu-id="de72f-112">PARAMETERS</span></span>

### <span data-ttu-id="de72f-113">-Force</span><span class="sxs-lookup"><span data-stu-id="de72f-113">-Force</span></span>
<span data-ttu-id="de72f-114">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="de72f-114">Forces the command to run without asking for user confirmation.</span></span>

<span data-ttu-id="de72f-115">Use esse sinalizador para ignorar mensagens de aviso ao remover a associação de IP reservado.</span><span class="sxs-lookup"><span data-stu-id="de72f-115">Use this flag to bypass warning messages when removing the reserved IP association.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de72f-116">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="de72f-116">-InformationAction</span></span>
<span data-ttu-id="de72f-117">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="de72f-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="de72f-118">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="de72f-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="de72f-119">Contínuo</span><span class="sxs-lookup"><span data-stu-id="de72f-119">Continue</span></span>
- <span data-ttu-id="de72f-120">Ignorar</span><span class="sxs-lookup"><span data-stu-id="de72f-120">Ignore</span></span>
- <span data-ttu-id="de72f-121">Inquire</span><span class="sxs-lookup"><span data-stu-id="de72f-121">Inquire</span></span>
- <span data-ttu-id="de72f-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="de72f-122">SilentlyContinue</span></span>
- <span data-ttu-id="de72f-123">Finaliza</span><span class="sxs-lookup"><span data-stu-id="de72f-123">Stop</span></span>
- <span data-ttu-id="de72f-124">Suspensão</span><span class="sxs-lookup"><span data-stu-id="de72f-124">Suspend</span></span>

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

### <span data-ttu-id="de72f-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="de72f-125">-InformationVariable</span></span>
<span data-ttu-id="de72f-126">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="de72f-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="de72f-127">-Perfil</span><span class="sxs-lookup"><span data-stu-id="de72f-127">-Profile</span></span>
<span data-ttu-id="de72f-128">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="de72f-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="de72f-129">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="de72f-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="de72f-130">-ReservedIPName</span><span class="sxs-lookup"><span data-stu-id="de72f-130">-ReservedIPName</span></span>
<span data-ttu-id="de72f-131">Especifica o nome do endereço IP reservado.</span><span class="sxs-lookup"><span data-stu-id="de72f-131">Specifies the name of the reserved IP address.</span></span>

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

### <span data-ttu-id="de72f-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="de72f-132">-ServiceName</span></span>
<span data-ttu-id="de72f-133">Especifica o nome do serviço.</span><span class="sxs-lookup"><span data-stu-id="de72f-133">Specifies the  name of the service.</span></span>

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

### <span data-ttu-id="de72f-134">-Slot</span><span class="sxs-lookup"><span data-stu-id="de72f-134">-Slot</span></span>
<span data-ttu-id="de72f-135">Especifica o ambiente de implantação.</span><span class="sxs-lookup"><span data-stu-id="de72f-135">Specifies the deployment environment.</span></span>
<span data-ttu-id="de72f-136">Os valores aceitáveis para esse parâmetro são: produção, preparação.</span><span class="sxs-lookup"><span data-stu-id="de72f-136">The acceptable values for this parameter are: Production, Staging.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de72f-137">-VirtualIPName</span><span class="sxs-lookup"><span data-stu-id="de72f-137">-VirtualIPName</span></span>
<span data-ttu-id="de72f-138">Especifica um endereço IP virtual do qual você deseja remover a associação com um serviço ou uma VM.</span><span class="sxs-lookup"><span data-stu-id="de72f-138">Specifies a virtual IP address from which to remove the association with a service or VM.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de72f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de72f-139">CommonParameters</span></span>
<span data-ttu-id="de72f-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de72f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de72f-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de72f-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de72f-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="de72f-142">INPUTS</span></span>

## <span data-ttu-id="de72f-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="de72f-143">OUTPUTS</span></span>

### <span data-ttu-id="de72f-144">Microsoft. WindowsAzure. Commands. Utilities. Common. ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="de72f-144">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="de72f-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="de72f-145">NOTES</span></span>

## <span data-ttu-id="de72f-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="de72f-146">RELATED LINKS</span></span>

[<span data-ttu-id="de72f-147">Set-AzureReservedIPAssociation</span><span class="sxs-lookup"><span data-stu-id="de72f-147">Set-AzureReservedIPAssociation</span></span>](./Set-AzureReservedIPAssociation.md)


