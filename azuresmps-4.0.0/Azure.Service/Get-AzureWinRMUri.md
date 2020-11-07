---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 5F827BFB-492E-48A2-9610-0CB5FBDD1F9E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0c66043fa36620c2879e88b7dbf82ba251aa4fbc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946505"
---
# <span data-ttu-id="7c74c-101">Get-AzureWinRMUri</span><span class="sxs-lookup"><span data-stu-id="7c74c-101">Get-AzureWinRMUri</span></span>

## <span data-ttu-id="7c74c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7c74c-102">SYNOPSIS</span></span>
<span data-ttu-id="7c74c-103">Obtém o URI para o ouvinte de HTTPS do WinRM para uma máquina virtual ou uma lista de máquinas virtuais em um serviço hospedado.</span><span class="sxs-lookup"><span data-stu-id="7c74c-103">Gets the URI to WinRM https listener to a virtual machine or a list of virtual machines in a hosted service.</span></span>

## <span data-ttu-id="7c74c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7c74c-104">SYNTAX</span></span>

```
Get-AzureWinRMUri [-ServiceName] <String> [[-Name] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="7c74c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7c74c-105">DESCRIPTION</span></span>
<span data-ttu-id="7c74c-106">O cmdlet **Get-AzureWinRMUri** Obtém o URI do ouvinte HTTPS do Windows Remote Management (WinRM) para uma máquina virtual ou uma lista de máquinas virtuais em um serviço hospedado.</span><span class="sxs-lookup"><span data-stu-id="7c74c-106">The **Get-AzureWinRMUri** cmdlet gets the URI of the Windows Remote Management (WinRM) https listener to a virtual machine or a list of virtual machines in a hosted service.</span></span>

## <span data-ttu-id="7c74c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7c74c-107">EXAMPLES</span></span>

### <span data-ttu-id="7c74c-108">Exemplo 1: obter o URI do ouvinte de HTTPS do WinRM para uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="7c74c-108">Example 1: Get the URI of the WinRM https listener to a virtual machine</span></span>
```
PS C:\> Get-AzureWinRMUri -ServiceName MyService -Name MyVM
```

<span data-ttu-id="7c74c-109">Esse comando obtém o UIR do ouvinte de HTTPS de WinRM para uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="7c74c-109">This command gets the UIR of the WinRM https listener to a virtual machine.</span></span>

### <span data-ttu-id="7c74c-110">Exemplo 2: obter o URI do ouvinte de HTTPS do WinRM para uma máquina virtual de um serviço específico</span><span class="sxs-lookup"><span data-stu-id="7c74c-110">Example 2: Get the URI of the WinRM https listener to a virtual machine of a specific service</span></span>
```
PS C:\> Get-AzureWinRMUri -ServiceName MyService
```

<span data-ttu-id="7c74c-111">Esse comando obtém o UIR do ouvinte de HTTPS de WinRM para uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="7c74c-111">This command gets the UIR of the WinRM https listener to a virtual machine.</span></span>

## <span data-ttu-id="7c74c-112">OS</span><span class="sxs-lookup"><span data-stu-id="7c74c-112">PARAMETERS</span></span>

### <span data-ttu-id="7c74c-113">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="7c74c-113">-InformationAction</span></span>
<span data-ttu-id="7c74c-114">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="7c74c-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="7c74c-115">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="7c74c-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7c74c-116">Contínuo</span><span class="sxs-lookup"><span data-stu-id="7c74c-116">Continue</span></span>
- <span data-ttu-id="7c74c-117">Ignorar</span><span class="sxs-lookup"><span data-stu-id="7c74c-117">Ignore</span></span>
- <span data-ttu-id="7c74c-118">Inquire</span><span class="sxs-lookup"><span data-stu-id="7c74c-118">Inquire</span></span>
- <span data-ttu-id="7c74c-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="7c74c-119">SilentlyContinue</span></span>
- <span data-ttu-id="7c74c-120">Finaliza</span><span class="sxs-lookup"><span data-stu-id="7c74c-120">Stop</span></span>
- <span data-ttu-id="7c74c-121">Suspensão</span><span class="sxs-lookup"><span data-stu-id="7c74c-121">Suspend</span></span>

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

### <span data-ttu-id="7c74c-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="7c74c-122">-InformationVariable</span></span>
<span data-ttu-id="7c74c-123">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="7c74c-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="7c74c-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="7c74c-124">-Name</span></span>
<span data-ttu-id="7c74c-125">Especifica o nome da máquina virtual para a qual o URI do WinRM é gerado.</span><span class="sxs-lookup"><span data-stu-id="7c74c-125">Specifies the name of the virtual machine to which the WinRM URI is generated.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c74c-126">-Perfil</span><span class="sxs-lookup"><span data-stu-id="7c74c-126">-Profile</span></span>
<span data-ttu-id="7c74c-127">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="7c74c-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7c74c-128">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="7c74c-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7c74c-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="7c74c-129">-ServiceName</span></span>
<span data-ttu-id="7c74c-130">Especifica o nome do serviço do Microsoft Azure que hospeda a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="7c74c-130">Specifies the name of the Microsoft Azure service that hosts the virtual machine.</span></span>

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

### <span data-ttu-id="7c74c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c74c-131">CommonParameters</span></span>
<span data-ttu-id="7c74c-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c74c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c74c-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c74c-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c74c-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7c74c-134">INPUTS</span></span>

## <span data-ttu-id="7c74c-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7c74c-135">OUTPUTS</span></span>

## <span data-ttu-id="7c74c-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7c74c-136">NOTES</span></span>

## <span data-ttu-id="7c74c-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7c74c-137">RELATED LINKS</span></span>

[<span data-ttu-id="7c74c-138">New-AzureVM</span><span class="sxs-lookup"><span data-stu-id="7c74c-138">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="7c74c-139">New-AzureQuickVM</span><span class="sxs-lookup"><span data-stu-id="7c74c-139">New-AzureQuickVM</span></span>](./New-AzureQuickVM.md)


