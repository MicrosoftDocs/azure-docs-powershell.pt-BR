---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1CFB90FD-7BC5-4687-8D08-775097DDA062
online version: ''
schema: 2.0.0
ms.openlocfilehash: 651b38a21dff03ce3c5925040d65bc2967eeaa77
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945645"
---
# <span data-ttu-id="8b5ab-101">Get-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="8b5ab-101">Get-AzureEndpoint</span></span>

## <span data-ttu-id="8b5ab-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8b5ab-102">SYNOPSIS</span></span>
<span data-ttu-id="8b5ab-103">Obtém informações sobre os pontos de extremidade atribuídos a uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="8b5ab-103">Gets information about the endpoints that are assigned to an Azure virtual machine.</span></span>

## <span data-ttu-id="8b5ab-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8b5ab-104">SYNTAX</span></span>

```
Get-AzureEndpoint [[-Name] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="8b5ab-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8b5ab-105">DESCRIPTION</span></span>
<span data-ttu-id="8b5ab-106">O cmdlet **Get-AzureEndpoint** Obtém informações sobre os pontos de extremidade atribuídos a uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="8b5ab-106">The **Get-AzureEndpoint** cmdlet gets information about the endpoints that are assigned to an Azure virtual machine.</span></span>

## <span data-ttu-id="8b5ab-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8b5ab-107">EXAMPLES</span></span>

### <span data-ttu-id="8b5ab-108">Exemplo 1: obter informações de ponto de extremidade para uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="8b5ab-108">Example 1: Get endpoint information for a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine12" | Get-AzureEndpoint
```

<span data-ttu-id="8b5ab-109">Esse comando recupera a configuração de uma máquina virtual nomeada VirtualMachine12 usando o cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="8b5ab-109">This command retrieves the configuration of a virtual machine named VirtualMachine12 by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="8b5ab-110">O comando passa a ele para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="8b5ab-110">The command passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="8b5ab-111">Este cmdlet obtém informações de ponto de extremidade para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8b5ab-111">This cmdlet gets endpoint information for that virtual machine.</span></span>

## <span data-ttu-id="8b5ab-112">OS</span><span class="sxs-lookup"><span data-stu-id="8b5ab-112">PARAMETERS</span></span>

### <span data-ttu-id="8b5ab-113">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="8b5ab-113">-InformationAction</span></span>
<span data-ttu-id="8b5ab-114">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="8b5ab-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="8b5ab-115">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="8b5ab-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8b5ab-116">Contínuo</span><span class="sxs-lookup"><span data-stu-id="8b5ab-116">Continue</span></span>
- <span data-ttu-id="8b5ab-117">Ignorar</span><span class="sxs-lookup"><span data-stu-id="8b5ab-117">Ignore</span></span>
- <span data-ttu-id="8b5ab-118">Inquire</span><span class="sxs-lookup"><span data-stu-id="8b5ab-118">Inquire</span></span>
- <span data-ttu-id="8b5ab-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="8b5ab-119">SilentlyContinue</span></span>
- <span data-ttu-id="8b5ab-120">Finaliza</span><span class="sxs-lookup"><span data-stu-id="8b5ab-120">Stop</span></span>
- <span data-ttu-id="8b5ab-121">Suspensão</span><span class="sxs-lookup"><span data-stu-id="8b5ab-121">Suspend</span></span>

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

### <span data-ttu-id="8b5ab-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="8b5ab-122">-InformationVariable</span></span>
<span data-ttu-id="8b5ab-123">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="8b5ab-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="8b5ab-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="8b5ab-124">-Name</span></span>
<span data-ttu-id="8b5ab-125">Especifica o nome do ponto de extremidade para o qual este cmdlet obtém informações.</span><span class="sxs-lookup"><span data-stu-id="8b5ab-125">Specifies the name of the endpoint for which this cmdlet gets information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b5ab-126">-Perfil</span><span class="sxs-lookup"><span data-stu-id="8b5ab-126">-Profile</span></span>
<span data-ttu-id="8b5ab-127">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="8b5ab-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8b5ab-128">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="8b5ab-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8b5ab-129">-VM</span><span class="sxs-lookup"><span data-stu-id="8b5ab-129">-VM</span></span>
<span data-ttu-id="8b5ab-130">Especifica a máquina virtual a partir da qual esse cmdlet obtém informações de ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="8b5ab-130">Specifies the virtual machine from which this cmdlet gets endpoint information.</span></span>

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

### <span data-ttu-id="8b5ab-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b5ab-131">CommonParameters</span></span>
<span data-ttu-id="8b5ab-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b5ab-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b5ab-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b5ab-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b5ab-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8b5ab-134">INPUTS</span></span>

## <span data-ttu-id="8b5ab-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8b5ab-135">OUTPUTS</span></span>

## <span data-ttu-id="8b5ab-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8b5ab-136">NOTES</span></span>

## <span data-ttu-id="8b5ab-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8b5ab-137">RELATED LINKS</span></span>

[<span data-ttu-id="8b5ab-138">Add-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="8b5ab-138">Add-AzureEndpoint</span></span>](./Add-AzureEndpoint.md)

[<span data-ttu-id="8b5ab-139">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="8b5ab-139">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="8b5ab-140">Remove-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="8b5ab-140">Remove-AzureEndpoint</span></span>](./Remove-AzureEndpoint.md)

[<span data-ttu-id="8b5ab-141">Set-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="8b5ab-141">Set-AzureEndpoint</span></span>](./Set-AzureEndpoint.md)


