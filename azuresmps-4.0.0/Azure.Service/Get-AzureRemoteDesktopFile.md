---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 8A6B2633-EECC-416A-85F6-69C8341AA970
online version: ''
schema: 2.0.0
ms.openlocfilehash: 82ef50dcdf5f17e044a9dc2091cbfda5cb5d1b2a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945620"
---
# <span data-ttu-id="ee8d1-101">Get-AzureRemoteDesktopFile</span><span class="sxs-lookup"><span data-stu-id="ee8d1-101">Get-AzureRemoteDesktopFile</span></span>

## <span data-ttu-id="ee8d1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ee8d1-102">SYNOPSIS</span></span>
<span data-ttu-id="ee8d1-103">Obtém um arquivo RDP para uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="ee8d1-103">Gets an RDP file for an Azure virtual machine.</span></span>

## <span data-ttu-id="ee8d1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ee8d1-104">SYNTAX</span></span>

### <span data-ttu-id="ee8d1-105">Baixar (padrão)</span><span class="sxs-lookup"><span data-stu-id="ee8d1-105">Download (Default)</span></span>
```
Get-AzureRemoteDesktopFile [-Name] <String> [-LocalPath] <String> [-ServiceName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="ee8d1-106">Carregar</span><span class="sxs-lookup"><span data-stu-id="ee8d1-106">Launch</span></span>
```
Get-AzureRemoteDesktopFile [-Name] <String> [[-LocalPath] <String>] [-Launch] [-ServiceName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="ee8d1-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ee8d1-107">DESCRIPTION</span></span>
<span data-ttu-id="ee8d1-108">O cmdlet **Get-AzureRemoteDesktopFile** baixa e salva um arquivo RDP (conexão de área de trabalho remota) para uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="ee8d1-108">The **Get-AzureRemoteDesktopFile** cmdlet downloads and saves a remote desktop connection (RDP) file for an Azure virtual machine.</span></span>
<span data-ttu-id="ee8d1-109">O cmdlet pode iniciar uma conexão de área de trabalho remota para a máquina virtual especificada.</span><span class="sxs-lookup"><span data-stu-id="ee8d1-109">The cmdlet can launch a remote desktop connection to the specified virtual machine.</span></span>

## <span data-ttu-id="ee8d1-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ee8d1-110">EXAMPLES</span></span>

### <span data-ttu-id="ee8d1-111">Exemplo 1: obter um arquivo RDP</span><span class="sxs-lookup"><span data-stu-id="ee8d1-111">Example 1: Get an RDP file</span></span>
```
PS C:\> Get-AzureRemoteDesktopFile -ServiceName "ContosoService" -Name "VirtualMachine07" -LocalPath "C:\temp\VirtualMachine07.rdp"
```

<span data-ttu-id="ee8d1-112">Esse comando obtém um arquivo RDP para a máquina virtual VirtualMachine07 chamada VirtualMachine07 que é executada no serviço denominado ContosoService.</span><span class="sxs-lookup"><span data-stu-id="ee8d1-112">This command gets an RDP file for the VirtualMachine07 virtual machine named VirtualMachine07 that runs on the service named ContosoService.</span></span>
<span data-ttu-id="ee8d1-113">O comando armazena esse arquivo como C:\temp\VirtualMachine07.rdp.</span><span class="sxs-lookup"><span data-stu-id="ee8d1-113">The command stores that file as C:\temp\VirtualMachine07.rdp.</span></span>

### <span data-ttu-id="ee8d1-114">Exemplo 2: iniciar uma sessão remota</span><span class="sxs-lookup"><span data-stu-id="ee8d1-114">Example 2: Start a remote session</span></span>
```
PS C:\> Get-AzureRemoteDesktopFile -ServiceName "ContosoService" -Name "VirtualMachine07" -Launch
```

<span data-ttu-id="ee8d1-115">Esse comando obtém um arquivo RDP para a máquina virtual VirtualMachine07 chamada VirtualMachine07 que é executada no serviço denominado ContosoService.</span><span class="sxs-lookup"><span data-stu-id="ee8d1-115">This command gets an RDP file for the VirtualMachine07 virtual machine named VirtualMachine07 that runs on the service named ContosoService.</span></span>
<span data-ttu-id="ee8d1-116">O comando inicia uma sessão de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="ee8d1-116">The command launches a remote desktop session.</span></span>
<span data-ttu-id="ee8d1-117">O comando exclui o arquivo RDP quando a conexão é fechada.</span><span class="sxs-lookup"><span data-stu-id="ee8d1-117">The command deletes the RDP file when the connection is closed.</span></span>

## <span data-ttu-id="ee8d1-118">OS</span><span class="sxs-lookup"><span data-stu-id="ee8d1-118">PARAMETERS</span></span>

### <span data-ttu-id="ee8d1-119">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="ee8d1-119">-InformationAction</span></span>
<span data-ttu-id="ee8d1-120">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="ee8d1-120">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ee8d1-121">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="ee8d1-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ee8d1-122">Contínuo</span><span class="sxs-lookup"><span data-stu-id="ee8d1-122">Continue</span></span>
- <span data-ttu-id="ee8d1-123">Ignorar</span><span class="sxs-lookup"><span data-stu-id="ee8d1-123">Ignore</span></span>
- <span data-ttu-id="ee8d1-124">Inquire</span><span class="sxs-lookup"><span data-stu-id="ee8d1-124">Inquire</span></span>
- <span data-ttu-id="ee8d1-125">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ee8d1-125">SilentlyContinue</span></span>
- <span data-ttu-id="ee8d1-126">Finaliza</span><span class="sxs-lookup"><span data-stu-id="ee8d1-126">Stop</span></span>
- <span data-ttu-id="ee8d1-127">Suspensão</span><span class="sxs-lookup"><span data-stu-id="ee8d1-127">Suspend</span></span>

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

### <span data-ttu-id="ee8d1-128">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ee8d1-128">-InformationVariable</span></span>
<span data-ttu-id="ee8d1-129">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="ee8d1-129">Specifies an information variable.</span></span>

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

### <span data-ttu-id="ee8d1-130">-Iniciar</span><span class="sxs-lookup"><span data-stu-id="ee8d1-130">-Launch</span></span>
<span data-ttu-id="ee8d1-131">Indica que esse cmdlet inicia uma sessão da área de trabalho remota para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ee8d1-131">Indicates that this cmdlet starts a remote desktop session to the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Launch
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee8d1-132">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="ee8d1-132">-LocalPath</span></span>
<span data-ttu-id="ee8d1-133">Especifica o caminho completo do arquivo RDP baixado no computador local.</span><span class="sxs-lookup"><span data-stu-id="ee8d1-133">Specifies the full path of the downloaded RDP file on the local computer.</span></span>

```yaml
Type: String
Parameter Sets: Download
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Launch
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee8d1-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="ee8d1-134">-Name</span></span>
<span data-ttu-id="ee8d1-135">Especifica a máquina virtual para a qual esse cmdlet baixa um arquivo RDP.</span><span class="sxs-lookup"><span data-stu-id="ee8d1-135">Specifies the virtual machine for which this cmdlet downloads an RDP file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: InstanceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee8d1-136">-Perfil</span><span class="sxs-lookup"><span data-stu-id="ee8d1-136">-Profile</span></span>
<span data-ttu-id="ee8d1-137">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="ee8d1-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ee8d1-138">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="ee8d1-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ee8d1-139">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="ee8d1-139">-ServiceName</span></span>
<span data-ttu-id="ee8d1-140">Especifica o nome do serviço do Azure ao qual a máquina virtual pertence.</span><span class="sxs-lookup"><span data-stu-id="ee8d1-140">Specifies the name of the Azure service to which the virtual machine belongs.</span></span>

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

### <span data-ttu-id="ee8d1-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee8d1-141">CommonParameters</span></span>
<span data-ttu-id="ee8d1-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee8d1-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee8d1-143">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee8d1-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee8d1-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ee8d1-144">INPUTS</span></span>

## <span data-ttu-id="ee8d1-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ee8d1-145">OUTPUTS</span></span>

## <span data-ttu-id="ee8d1-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ee8d1-146">NOTES</span></span>

## <span data-ttu-id="ee8d1-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ee8d1-147">RELATED LINKS</span></span>

