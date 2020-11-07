---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: CE1C6576-234E-4891-9158-FA45B64B786C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 41e8641b01dcb95a6b6939ff3551fe03b642ddf0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945435"
---
# <span data-ttu-id="3f508-101">Set-AzureStorSimpleVirtualDevice</span><span class="sxs-lookup"><span data-stu-id="3f508-101">Set-AzureStorSimpleVirtualDevice</span></span>

## <span data-ttu-id="3f508-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3f508-102">SYNOPSIS</span></span>
<span data-ttu-id="3f508-103">Cria ou atualiza a configuração do dispositivo de um dispositivo virtual StorSimple.</span><span class="sxs-lookup"><span data-stu-id="3f508-103">Creates or updates the device configuration of a StorSimple virtual device.</span></span>

## <span data-ttu-id="3f508-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3f508-104">SYNTAX</span></span>

```
Set-AzureStorSimpleVirtualDevice -DeviceName <String> -SecretKey <String> -AdministratorPassword <String>
 -SnapshotManagerPassword <String> [-TimeZone <TimeZoneInfo>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3f508-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3f508-105">DESCRIPTION</span></span>
<span data-ttu-id="3f508-106">O cmdlet **set-AzureStorSimpleVirtualDevice** cria ou atualiza a configuração do dispositivo de um dispositivo virtual Azure StorSimple.</span><span class="sxs-lookup"><span data-stu-id="3f508-106">The **Set-AzureStorSimpleVirtualDevice** cmdlet creates or updates the device configuration of an Azure StorSimple virtual device.</span></span>

## <span data-ttu-id="3f508-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3f508-107">EXAMPLES</span></span>

### <span data-ttu-id="3f508-108">Exemplo 1: atualizar um dispositivo virtual</span><span class="sxs-lookup"><span data-stu-id="3f508-108">Example 1: Update a virtual device</span></span>
```
PS C:\>$TimeZoneInfo = [System.TimeZoneInfo]::GetSystemTimeZones() | where { $_.Id -eq "Pacific Standard Time" }
PS C:\> Set-AzureStorSimpleVirtualDevice -DeviceName "Contoso23" -SecretKey "wcZBlBGpCMf4USdSKyt/SQ==" -TimeZone $TimeZoneInfo
VERBOSE: ClientRequestId: e31f0d6b-451d-4c1d-b2f1-3fc84c13972c_PS
VERBOSE: ClientRequestId: df58db83-d563-4a2e-bbb4-9576f0e69ca6_PS
VERBOSE: ClientRequestId: 494a9f0d-79ee-4fde-ab4d-85ee5a357556_PS
VERBOSE: ClientRequestId: ce557cbf-174d-4301-93d4-5ffe082c8413_PS
VERBOSE: ClientRequestId: 31284dad-de2c-4758-a2ef-45962875bfa6_PS
VERBOSE: About to configure the device : win-ff93i74m1e1 ! 
VERBOSE: ClientRequestId: d9c66302-45d8-488a-adda-8ccf957f77d3_PS


TaskId       : 21f530c3-bc47-4591-8c4e-da4d694b751d
TaskResult   : Succeeded
TaskStatus   : Completed
ErrorCode    : 
ErrorMessage : 
TaskSteps    : {Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep, Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep}

VERBOSE: The task created for your Setup operation has completed successfully. 
VERBOSE: ClientRequestId: a94f972c-18ea-40b6-9401-2ad209c0c8b4_PS
AlertNotification              : Microsoft.WindowsAzure.Management.StorSimple.Models.AlertNotificationSettings
Chap                           : Microsoft.WindowsAzure.Management.StorSimple.Models.ChapSettings
DeviceProperties               : Microsoft.WindowsAzure.Management.StorSimple.Models.DeviceInfo
DnsServer                      : Microsoft.WindowsAzure.Management.StorSimple.Models.DnsServerSettings
InstanceId                     : d369ebb4-8b9a-47fc-9a6b-60f371e123ae
Name                           : 
NetInterfaceList               : {}
OperationInProgress            : None
RemoteMgmtSettingsInfo         : Microsoft.WindowsAzure.Management.StorSimple.Models.RemoteManagementSettings
RemoteMinishellSecretInfo      : Microsoft.WindowsAzure.Management.StorSimple.Models.RemoteMinishellSettings
SecretEncryptionCertThumbprint : 
Snapshot                       : Microsoft.WindowsAzure.Management.StorSimple.Models.SnapshotSettings
TimeServer                     : Microsoft.WindowsAzure.Management.StorSimple.Models.TimeSettings
Type                           : VirtualAppliance
VirtualApplianceProperties     : Microsoft.WindowsAzure.Management.StorSimple.Models.VirtualApplianceInfo
WebProxy                       : Microsoft.WindowsAzure.Management.StorSimple.Models.WebProxySettings

VERBOSE: Successfully updated configuration for device Contoso23 with id d369ebb4-8b9a-47fc-9a6b-60f371e123ae
```

<span data-ttu-id="3f508-109">O primeiro comando usa a classe **System. TimeZoneInfo** do .net e a sintaxe padrão para obter o fuso horário padrão do Pacífico e armazena esse objeto na variável $TimeZoneInfo.</span><span class="sxs-lookup"><span data-stu-id="3f508-109">The first command uses the **System.TimeZoneInfo** .NET class and standard syntax to get Pacific Standard Time zone, and stores that object in the $TimeZoneInfo variable.</span></span>

<span data-ttu-id="3f508-110">O segundo comando atualiza o dispositivo chamado Contoso23 para usar o fuso horário especificado em $TimeZoneInfo.</span><span class="sxs-lookup"><span data-stu-id="3f508-110">The second command updates the device named Contoso23 to use the time zone specified in $TimeZoneInfo.</span></span>
<span data-ttu-id="3f508-111">O comando requer a chave secreta para acessar a configuração do dispositivo virtual.</span><span class="sxs-lookup"><span data-stu-id="3f508-111">The command requires the secret key to access the virtual device configuration.</span></span>

### <span data-ttu-id="3f508-112">Exemplo 2: atualizar um dispositivo virtual usando o operador pipeline</span><span class="sxs-lookup"><span data-stu-id="3f508-112">Example 2: Update a virtual device by using the pipeline operator</span></span>
```
PS C:\> [System.TimeZoneInfo]::GetSystemTimeZones() | where { $_.Id -eq "Pacific Standard Time" } | Set-AzureStorSimpleVirtualDevice -DeviceName "Contoso23" -SecretKey "wcZBlBGpCMf4USdSKyt/SQ=="
```

<span data-ttu-id="3f508-113">Esse comando atualiza o dispositivo chamado Contoso23 para usar o fuso horário criado pelo comando.</span><span class="sxs-lookup"><span data-stu-id="3f508-113">This command updates the device named Contoso23 to use the time zone that the command creates.</span></span>
<span data-ttu-id="3f508-114">O comando requer a chave secreta para acessar a configuração do dispositivo virtual.</span><span class="sxs-lookup"><span data-stu-id="3f508-114">The command requires the secret key to access the virtual device configuration.</span></span>
<span data-ttu-id="3f508-115">Esse comando funciona da mesma maneira que o exemplo anterior, exceto que ele passa o fuso horário para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="3f508-115">This command works the same way as the previous example, except that it passes the time zone to the current cmdlet by using the pipeline operator.</span></span>

## <span data-ttu-id="3f508-116">OS</span><span class="sxs-lookup"><span data-stu-id="3f508-116">PARAMETERS</span></span>

### <span data-ttu-id="3f508-117">-AdministratorPassword</span><span class="sxs-lookup"><span data-stu-id="3f508-117">-AdministratorPassword</span></span>
<span data-ttu-id="3f508-118">Especifica a senha de administrador do dispositivo virtual a ser configurado.</span><span class="sxs-lookup"><span data-stu-id="3f508-118">Specifies the administrator password of the virtual device to configure.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f508-119">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="3f508-119">-DeviceName</span></span>
<span data-ttu-id="3f508-120">Especifica o nome do dispositivo virtual a ser configurado.</span><span class="sxs-lookup"><span data-stu-id="3f508-120">Specifies the name of the virtual device to configure.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f508-121">-Perfil</span><span class="sxs-lookup"><span data-stu-id="3f508-121">-Profile</span></span>
<span data-ttu-id="3f508-122">Especifica um perfil do Azure.</span><span class="sxs-lookup"><span data-stu-id="3f508-122">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="3f508-123">-SecretKey</span><span class="sxs-lookup"><span data-stu-id="3f508-123">-SecretKey</span></span>
<span data-ttu-id="3f508-124">Especifica uma chave de criptografia de serviço para o dispositivo virtual.</span><span class="sxs-lookup"><span data-stu-id="3f508-124">Specifies a service encryption key for the virtual device.</span></span>
<span data-ttu-id="3f508-125">Essa chave é gerada quando o primeiro dispositivo físico é registrado com um recurso.</span><span class="sxs-lookup"><span data-stu-id="3f508-125">This key is generated when the first physical device is registered with a resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f508-126">-SnapshotManagerPassword</span><span class="sxs-lookup"><span data-stu-id="3f508-126">-SnapshotManagerPassword</span></span>
<span data-ttu-id="3f508-127">Especifica a senha do Gerenciador de instantâneos.</span><span class="sxs-lookup"><span data-stu-id="3f508-127">Specifies the snapshot manager password.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f508-128">-Fuso horário</span><span class="sxs-lookup"><span data-stu-id="3f508-128">-TimeZone</span></span>
<span data-ttu-id="3f508-129">Especifica um fuso horário para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3f508-129">Specifies a time zone for the device.</span></span>
<span data-ttu-id="3f508-130">Você pode criar um objeto **TimeZoneInfo** usando o método **GetSystemTimeZone ()** .</span><span class="sxs-lookup"><span data-stu-id="3f508-130">You can create a **TimeZoneInfo** object by using the **GetSystemTimeZone()** method.</span></span>
<span data-ttu-id="3f508-131">Por exemplo, esse comando cria um objeto de informação de fuso horário para hora padrão do Pacífico: `\[System.TimeZoneInfo\]::GetSystemTimeZones() | where { $_.Id -eq "Pacific Standard Time" }`</span><span class="sxs-lookup"><span data-stu-id="3f508-131">For example, this command creates a time zone information object for Pacific Standard Time: `\[System.TimeZoneInfo\]::GetSystemTimeZones() | where { $_.Id -eq "Pacific Standard Time" }`</span></span>

```yaml
Type: TimeZoneInfo
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3f508-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f508-132">CommonParameters</span></span>
<span data-ttu-id="3f508-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f508-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f508-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f508-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f508-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3f508-135">INPUTS</span></span>

### <span data-ttu-id="3f508-136">TimeZoneInfo</span><span class="sxs-lookup"><span data-stu-id="3f508-136">TimeZoneInfo</span></span>
<span data-ttu-id="3f508-137">Você pode canalizar um objeto **TimeZoneInfo** para esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3f508-137">You can pipe a **TimeZoneInfo** object to this cmdlet.</span></span>

## <span data-ttu-id="3f508-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3f508-138">OUTPUTS</span></span>

### <span data-ttu-id="3f508-139">DeviceJobDetails</span><span class="sxs-lookup"><span data-stu-id="3f508-139">DeviceJobDetails</span></span>
<span data-ttu-id="3f508-140">Esse cmdlet retorna detalhes do dispositivo atualizado para o dispositivo virtual.</span><span class="sxs-lookup"><span data-stu-id="3f508-140">This cmdlet returns updated device details for the virtual device.</span></span>

## <span data-ttu-id="3f508-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3f508-141">NOTES</span></span>

## <span data-ttu-id="3f508-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3f508-142">RELATED LINKS</span></span>

[<span data-ttu-id="3f508-143">New-AzureStorSimpleVirtualDevice</span><span class="sxs-lookup"><span data-stu-id="3f508-143">New-AzureStorSimpleVirtualDevice</span></span>](./New-AzureStorSimpleVirtualDevice.md)

[<span data-ttu-id="3f508-144">Set-AzureStorSimpleDevice</span><span class="sxs-lookup"><span data-stu-id="3f508-144">Set-AzureStorSimpleDevice</span></span>](./Set-AzureStorSimpleDevice.md)


