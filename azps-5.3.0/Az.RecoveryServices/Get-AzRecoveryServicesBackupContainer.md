---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 1097FF29-1C23-4960-930C-5C1227419359
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupContainer.md
ms.openlocfilehash: 90532c6d314c78e6b7242ec480b95991138719de
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429691"
---
# <span data-ttu-id="05ae8-101">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="05ae8-101">Get-AzRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="05ae8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="05ae8-102">SYNOPSIS</span></span>

<span data-ttu-id="05ae8-103">Obtém contêineres de backup.</span><span class="sxs-lookup"><span data-stu-id="05ae8-103">Gets Backup containers.</span></span>

## <span data-ttu-id="05ae8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="05ae8-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupContainer [-ContainerType] <ContainerType> [[-BackupManagementType] <String>]
 [[-FriendlyName] <String>] [[-ResourceGroupName] <String>] [[-Status] <ContainerRegistrationStatus>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="05ae8-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="05ae8-105">DESCRIPTION</span></span>

<span data-ttu-id="05ae8-106">O cmdlet **Get-AzRecoveryServicesBackupContainer** Obtém um contêiner de backup.</span><span class="sxs-lookup"><span data-stu-id="05ae8-106">The **Get-AzRecoveryServicesBackupContainer** cmdlet gets a backup container.</span></span>
<span data-ttu-id="05ae8-107">Um contêiner de backup encapsula fontes de dados que são modelled como itens de backup.</span><span class="sxs-lookup"><span data-stu-id="05ae8-107">A Backup container encapsulates data sources that are modelled as backup items.</span></span>
<span data-ttu-id="05ae8-108">Defina o contexto do cofre usando o parâmetro-Cofreid.</span><span class="sxs-lookup"><span data-stu-id="05ae8-108">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="05ae8-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="05ae8-109">EXAMPLES</span></span>

### <span data-ttu-id="05ae8-110">Exemplo 1: obter um contêiner específico</span><span class="sxs-lookup"><span data-stu-id="05ae8-110">Example 1: Get a specific container</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupContainer -ContainerType "AzureVM" -Status "Registered" -FriendlyName "V2VM" -VaultId $vault.ID
```

<span data-ttu-id="05ae8-111">Esse comando obtém o contêiner chamado V2VM do tipo AzureVM.</span><span class="sxs-lookup"><span data-stu-id="05ae8-111">This command gets the container named V2VM of type AzureVM.</span></span>

### <span data-ttu-id="05ae8-112">Exemplo 2: obter todos os contêineres de um tipo específico</span><span class="sxs-lookup"><span data-stu-id="05ae8-112">Example 2: Get all containers of a specific type</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupContainer -ContainerType Windows -BackupManagementType MARS -VaultId $vault.ID
```

<span data-ttu-id="05ae8-113">Esse comando obtém todos os contêineres do Windows protegidos pelo agente de backup do Azure.</span><span class="sxs-lookup"><span data-stu-id="05ae8-113">This command gets all Windows containers that are protected by Azure Backup agent.</span></span>
<span data-ttu-id="05ae8-114">O parâmetro **BackupManagementType** é necessário apenas para contêineres do Windows.</span><span class="sxs-lookup"><span data-stu-id="05ae8-114">The **BackupManagementType** parameter is only required for Windows containers.</span></span>

## <span data-ttu-id="05ae8-115">OS</span><span class="sxs-lookup"><span data-stu-id="05ae8-115">PARAMETERS</span></span>

### <span data-ttu-id="05ae8-116">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="05ae8-116">-BackupManagementType</span></span>

<span data-ttu-id="05ae8-117">A classe de recursos que estão sendo protegidos.</span><span class="sxs-lookup"><span data-stu-id="05ae8-117">The class of resources being protected.</span></span> <span data-ttu-id="05ae8-118">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="05ae8-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="05ae8-119">AzureVM</span><span class="sxs-lookup"><span data-stu-id="05ae8-119">AzureVM</span></span>
- <span data-ttu-id="05ae8-120">Marte</span><span class="sxs-lookup"><span data-stu-id="05ae8-120">MARS</span></span>
- <span data-ttu-id="05ae8-121">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="05ae8-121">AzureWorkload</span></span>
- <span data-ttu-id="05ae8-122">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="05ae8-122">AzureStorage</span></span>

<span data-ttu-id="05ae8-123">Esse parâmetro é usado para diferenciar máquinas Windows que tenham o backup usando o agente MARS ou outros mecanismos de backup.</span><span class="sxs-lookup"><span data-stu-id="05ae8-123">This parameter is used to differentiate Windows machines that are backed up using MARS agent or other backup engines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, AzureWorkload, AzureStorage

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05ae8-124">-ContainerType</span><span class="sxs-lookup"><span data-stu-id="05ae8-124">-ContainerType</span></span>

<span data-ttu-id="05ae8-125">Especifica o tipo de contêiner de backup.</span><span class="sxs-lookup"><span data-stu-id="05ae8-125">Specifies the backup container type.</span></span>
<span data-ttu-id="05ae8-126">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="05ae8-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="05ae8-127">AzureVM</span><span class="sxs-lookup"><span data-stu-id="05ae8-127">AzureVM</span></span>
- <span data-ttu-id="05ae8-128">Windows</span><span class="sxs-lookup"><span data-stu-id="05ae8-128">Windows</span></span>
- <span data-ttu-id="05ae8-129">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="05ae8-129">AzureStorage</span></span>
- <span data-ttu-id="05ae8-130">AzureVMAppContainer</span><span class="sxs-lookup"><span data-stu-id="05ae8-130">AzureVMAppContainer</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, Windows, AzureStorage, AzureVMAppContainer

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05ae8-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05ae8-131">-DefaultProfile</span></span>

<span data-ttu-id="05ae8-132">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="05ae8-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05ae8-133">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="05ae8-133">-FriendlyName</span></span>

<span data-ttu-id="05ae8-134">Especifica o nome amigável do contêiner a obter.</span><span class="sxs-lookup"><span data-stu-id="05ae8-134">Specifies the friendly name of the container to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05ae8-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05ae8-135">-ResourceGroupName</span></span>

<span data-ttu-id="05ae8-136">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="05ae8-136">Specifies the name of the resource group.</span></span>
<span data-ttu-id="05ae8-137">Este parâmetro é somente para máquinas virtuais do Azure.</span><span class="sxs-lookup"><span data-stu-id="05ae8-137">This parameter is for Azure virtual machines only.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05ae8-138">-Status</span><span class="sxs-lookup"><span data-stu-id="05ae8-138">-Status</span></span>

<span data-ttu-id="05ae8-139">Especifica o status de registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="05ae8-139">Specifies the container registration status.</span></span>
<span data-ttu-id="05ae8-140">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="05ae8-140">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="05ae8-141">Removido</span><span class="sxs-lookup"><span data-stu-id="05ae8-141">Registered</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerRegistrationStatus
Parameter Sets: (All)
Aliases:
Accepted values: Registered

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05ae8-142">-Cofreid</span><span class="sxs-lookup"><span data-stu-id="05ae8-142">-VaultId</span></span>

<span data-ttu-id="05ae8-143">ID do braço do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="05ae8-143">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="05ae8-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05ae8-144">CommonParameters</span></span>
<span data-ttu-id="05ae8-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05ae8-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05ae8-146">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="05ae8-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05ae8-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="05ae8-147">INPUTS</span></span>

### <span data-ttu-id="05ae8-148">System. String</span><span class="sxs-lookup"><span data-stu-id="05ae8-148">System.String</span></span>

## <span data-ttu-id="05ae8-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="05ae8-149">OUTPUTS</span></span>

### <span data-ttu-id="05ae8-150">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="05ae8-150">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="05ae8-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="05ae8-151">NOTES</span></span>

## <span data-ttu-id="05ae8-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="05ae8-152">RELATED LINKS</span></span>

[<span data-ttu-id="05ae8-153">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="05ae8-153">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="05ae8-154">Get-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="05ae8-154">Get-AzRecoveryServicesBackupManagementServer</span></span>](./Get-AzRecoveryServicesBackupManagementServer.md)

[<span data-ttu-id="05ae8-155">Cancelar registro-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="05ae8-155">Unregister-AzRecoveryServicesBackupContainer</span></span>](./Unregister-AzRecoveryServicesBackupContainer.md)
