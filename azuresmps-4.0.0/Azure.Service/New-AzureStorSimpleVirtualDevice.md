---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: F16BCE0C-1F2C-4FB7-972D-28BE3CCD96D9
online version: ''
schema: 2.0.0
ms.openlocfilehash: dc41efa1901debf2efabf66f8d27f00da7eafe5f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945511"
---
# <span data-ttu-id="0777e-101">New-AzureStorSimpleVirtualDevice</span><span class="sxs-lookup"><span data-stu-id="0777e-101">New-AzureStorSimpleVirtualDevice</span></span>

## <span data-ttu-id="0777e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0777e-102">SYNOPSIS</span></span>
<span data-ttu-id="0777e-103">Cria um dispositivo virtual StorSimple.</span><span class="sxs-lookup"><span data-stu-id="0777e-103">Creates a virtual StorSimple device.</span></span>

## <span data-ttu-id="0777e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0777e-104">SYNTAX</span></span>

### <span data-ttu-id="0777e-105">CreateNewStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0777e-105">CreateNewStorageAccount</span></span>
```
New-AzureStorSimpleVirtualDevice -VirtualDeviceName <String> -VirtualNetworkName <String> -SubNetName <String>
 [-StorageAccountName <String>] [-CreateNewStorageAccount] [-PersistAzureVMOnFailrue]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="0777e-106">UseExistingStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0777e-106">UseExistingStorageAccount</span></span>
```
New-AzureStorSimpleVirtualDevice -VirtualDeviceName <String> -VirtualNetworkName <String> -SubNetName <String>
 -StorageAccountName <String> [-PersistAzureVMOnFailrue] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0777e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0777e-107">DESCRIPTION</span></span>
<span data-ttu-id="0777e-108">O cmdlet **New-AzureStorSimpleVirtualDevice** cria um dispositivo virtual StorSimple.</span><span class="sxs-lookup"><span data-stu-id="0777e-108">The **New-AzureStorSimpleVirtualDevice** cmdlet creates a virtual StorSimple device.</span></span>
<span data-ttu-id="0777e-109">Especifique um nome de dispositivo para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0777e-109">Specify a device name for the device.</span></span>
<span data-ttu-id="0777e-110">Especifique detalhes da rede virtual e da sub-rede para a rede virtual na mesma assinatura.</span><span class="sxs-lookup"><span data-stu-id="0777e-110">Specify virtual network and subnet details for the virtual network in the same subscription.</span></span>
<span data-ttu-id="0777e-111">A Geo deve corresponder à geográfica na qual o recurso StorSimple foi criado.</span><span class="sxs-lookup"><span data-stu-id="0777e-111">The geo should match the geo in which the StorSimple resource is created.</span></span>
<span data-ttu-id="0777e-112">Para usar uma conta de armazenamento existente para esse dispositivo virtual, especifique o nome.</span><span class="sxs-lookup"><span data-stu-id="0777e-112">To use an existing storage account for this virtual device, specify the name.</span></span>
<span data-ttu-id="0777e-113">Para criar uma nova conta de armazenamento para esse dispositivo virtual, especifique os parâmetros *StorageAccountName* e *CreateNewStorageAccount* .</span><span class="sxs-lookup"><span data-stu-id="0777e-113">To create a new storage account for this virtual device, specify both the *StorageAccountName* and the *CreateNewStorageAccount* parameters.</span></span>

## <span data-ttu-id="0777e-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0777e-114">EXAMPLES</span></span>

### <span data-ttu-id="0777e-115">Exemplo 1: criar um dispositivo virtual com uma nova conta e uma rede existente</span><span class="sxs-lookup"><span data-stu-id="0777e-115">Example 1: Create a virtual device with a new account and an existing network</span></span>
```
PS C:\>New-AzureStorSimpleVirtualDevice -VirtualDeviceName "Contosodevice02" -VirtualNetworkName "Saas2vpn" -SubNetName "TenantSubnet" -StorageAccountName "AzureTenant04" -CreateNewStorageAccount
64e4c564-b0ac-44b0-afb4-adf28ac24ad0
VERBOSE: The create job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId 64e4c564-b0ac-44b0-afb4-adf28ac24ad0 for tracking the job's status
```

<span data-ttu-id="0777e-116">Esse comando cria um dispositivo virtual que usa uma nova conta de armazenamento e uma rede virtual existente.</span><span class="sxs-lookup"><span data-stu-id="0777e-116">This command creates a virtual device that uses a new storage account and an existing virtual network.</span></span>

### <span data-ttu-id="0777e-117">Exemplo 2: criar um dispositivo virtual com uma conta existente e uma rede virtual</span><span class="sxs-lookup"><span data-stu-id="0777e-117">Example 2: Create a virtual device with an existing account and virtual network</span></span>
```
PS C:\>New-AzureStorSimpleVirtualDevice -VirtualDeviceName "ContosoDevice07" -VirtualNetworkName "Saas2vpn" -SubNetName TenantSubnet -StorageAccountName azurecisbvtdnd
2a18a3b7-1ec6-481d-b95d-66ba8f67ceaf
VERBOSE: The create job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId 2a18a3b7-1ec6-481d-b95d-66ba8f67ceaf for tracking the job's status
```

<span data-ttu-id="0777e-118">Esse comando cria um dispositivo virtual que usa uma conta de armazenamento existente e uma rede virtual existente.</span><span class="sxs-lookup"><span data-stu-id="0777e-118">This command creates a virtual device that uses an existing storage account and an existing virtual network.</span></span>

## <span data-ttu-id="0777e-119">OS</span><span class="sxs-lookup"><span data-stu-id="0777e-119">PARAMETERS</span></span>

### <span data-ttu-id="0777e-120">-CreateNewStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0777e-120">-CreateNewStorageAccount</span></span>
<span data-ttu-id="0777e-121">Indica que esse cmdlet cria uma nova conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="0777e-121">Indicates that this cmdlet creates a new storage account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: CreateNewStorageAccount
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0777e-122">-PersistAzureVMOnFailrue</span><span class="sxs-lookup"><span data-stu-id="0777e-122">-PersistAzureVMOnFailrue</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0777e-123">-Perfil</span><span class="sxs-lookup"><span data-stu-id="0777e-123">-Profile</span></span>
<span data-ttu-id="0777e-124">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="0777e-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0777e-125">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="0777e-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0777e-126">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="0777e-126">-StorageAccountName</span></span>
<span data-ttu-id="0777e-127">Especifica o nome de uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="0777e-127">Specifies the name of a storage account.</span></span>

```yaml
Type: String
Parameter Sets: CreateNewStorageAccount
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: UseExistingStorageAccount
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0777e-128">-SubNetname</span><span class="sxs-lookup"><span data-stu-id="0777e-128">-SubNetName</span></span>
<span data-ttu-id="0777e-129">Especifica o nome de uma sub-rede virtual.</span><span class="sxs-lookup"><span data-stu-id="0777e-129">Specifies the name of a virtual subnet.</span></span>

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

### <span data-ttu-id="0777e-130">-VirtualDeviceName</span><span class="sxs-lookup"><span data-stu-id="0777e-130">-VirtualDeviceName</span></span>
<span data-ttu-id="0777e-131">Especifica um nome para o dispositivo virtual.</span><span class="sxs-lookup"><span data-stu-id="0777e-131">Specifies a name for the virtual device.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0777e-132">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="0777e-132">-VirtualNetworkName</span></span>
<span data-ttu-id="0777e-133">Especifica o nome de uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="0777e-133">Specifies the name of a virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: VNetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0777e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0777e-134">CommonParameters</span></span>
<span data-ttu-id="0777e-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0777e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0777e-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0777e-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0777e-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0777e-137">INPUTS</span></span>

## <span data-ttu-id="0777e-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0777e-138">OUTPUTS</span></span>

### <span data-ttu-id="0777e-139">String</span><span class="sxs-lookup"><span data-stu-id="0777e-139">String</span></span>
<span data-ttu-id="0777e-140">Esse cmdlet retorna a ID do trabalho que cria o dispositivo virtual.</span><span class="sxs-lookup"><span data-stu-id="0777e-140">This cmdlet returns the ID of the job that creates the virtual device.</span></span>
<span data-ttu-id="0777e-141">Você pode usar essa ID para acompanhar o progresso usando o cmdlet Get-AzureStorSimpleJob.</span><span class="sxs-lookup"><span data-stu-id="0777e-141">You can use this ID to track the progress using the Get-AzureStorSimpleJob cmdlet.</span></span>

## <span data-ttu-id="0777e-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0777e-142">NOTES</span></span>

## <span data-ttu-id="0777e-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0777e-143">RELATED LINKS</span></span>

[<span data-ttu-id="0777e-144">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="0777e-144">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)

[<span data-ttu-id="0777e-145">Set-AzureStorSimpleVirtualDevice</span><span class="sxs-lookup"><span data-stu-id="0777e-145">Set-AzureStorSimpleVirtualDevice</span></span>](./Set-AzureStorSimpleVirtualDevice.md)


