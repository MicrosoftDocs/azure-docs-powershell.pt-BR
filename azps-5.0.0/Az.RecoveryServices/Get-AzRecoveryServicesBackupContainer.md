---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 1097FF29-1C23-4960-930C-5C1227419359
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupContainer.md
ms.openlocfilehash: f061dc0f729709dee3bfe08bb22dba8d49a7f31b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94281753"
---
# <span data-ttu-id="528bd-101">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="528bd-101">Get-AzRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="528bd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="528bd-102">SYNOPSIS</span></span>

<span data-ttu-id="528bd-103">Obtém contêineres de backup.</span><span class="sxs-lookup"><span data-stu-id="528bd-103">Gets Backup containers.</span></span>

## <span data-ttu-id="528bd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="528bd-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupContainer [-ContainerType] <ContainerType> [[-BackupManagementType] <String>]
 [[-FriendlyName] <String>] [[-ResourceGroupName] <String>] [[-Status] <ContainerRegistrationStatus>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="528bd-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="528bd-105">DESCRIPTION</span></span>

<span data-ttu-id="528bd-106">O cmdlet **Get-AzRecoveryServicesBackupContainer** Obtém um contêiner de backup.</span><span class="sxs-lookup"><span data-stu-id="528bd-106">The **Get-AzRecoveryServicesBackupContainer** cmdlet gets a backup container.</span></span>
<span data-ttu-id="528bd-107">Um contêiner de backup encapsula fontes de dados que são modelled como itens de backup.</span><span class="sxs-lookup"><span data-stu-id="528bd-107">A Backup container encapsulates data sources that are modelled as backup items.</span></span>
<span data-ttu-id="528bd-108">Defina o contexto do cofre usando o parâmetro-Cofreid.</span><span class="sxs-lookup"><span data-stu-id="528bd-108">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="528bd-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="528bd-109">EXAMPLES</span></span>

### <span data-ttu-id="528bd-110">Exemplo 1: obter um contêiner específico</span><span class="sxs-lookup"><span data-stu-id="528bd-110">Example 1: Get a specific container</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupContainer -ContainerType "AzureVM" -Status "Registered" -FriendlyName "V2VM" -VaultId $vault.ID
```

<span data-ttu-id="528bd-111">Esse comando obtém o contêiner chamado V2VM do tipo AzureVM.</span><span class="sxs-lookup"><span data-stu-id="528bd-111">This command gets the container named V2VM of type AzureVM.</span></span>

### <span data-ttu-id="528bd-112">Exemplo 2: obter todos os contêineres de um tipo específico</span><span class="sxs-lookup"><span data-stu-id="528bd-112">Example 2: Get all containers of a specific type</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupContainer -ContainerType Windows -BackupManagementType MARS -VaultId $vault.ID
```

<span data-ttu-id="528bd-113">Esse comando obtém todos os contêineres do Windows protegidos pelo agente de backup do Azure.</span><span class="sxs-lookup"><span data-stu-id="528bd-113">This command gets all Windows containers that are protected by Azure Backup agent.</span></span>
<span data-ttu-id="528bd-114">O parâmetro **BackupManagementType** é necessário apenas para contêineres do Windows.</span><span class="sxs-lookup"><span data-stu-id="528bd-114">The **BackupManagementType** parameter is only required for Windows containers.</span></span>

## <span data-ttu-id="528bd-115">OS</span><span class="sxs-lookup"><span data-stu-id="528bd-115">PARAMETERS</span></span>

### <span data-ttu-id="528bd-116">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="528bd-116">-BackupManagementType</span></span>

<span data-ttu-id="528bd-117">A classe de recursos que estão sendo protegidos.</span><span class="sxs-lookup"><span data-stu-id="528bd-117">The class of resources being protected.</span></span> <span data-ttu-id="528bd-118">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="528bd-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="528bd-119">AzureVM</span><span class="sxs-lookup"><span data-stu-id="528bd-119">AzureVM</span></span>
- <span data-ttu-id="528bd-120">Marte</span><span class="sxs-lookup"><span data-stu-id="528bd-120">MARS</span></span>
- <span data-ttu-id="528bd-121">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="528bd-121">AzureWorkload</span></span>
- <span data-ttu-id="528bd-122">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="528bd-122">AzureStorage</span></span>

<span data-ttu-id="528bd-123">Esse parâmetro é usado para diferenciar máquinas Windows que tenham o backup usando o agente MARS ou outros mecanismos de backup.</span><span class="sxs-lookup"><span data-stu-id="528bd-123">This parameter is used to differentiate Windows machines that are backed up using MARS agent or other backup engines.</span></span>

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

### <span data-ttu-id="528bd-124">-ContainerType</span><span class="sxs-lookup"><span data-stu-id="528bd-124">-ContainerType</span></span>

<span data-ttu-id="528bd-125">Especifica o tipo de contêiner de backup.</span><span class="sxs-lookup"><span data-stu-id="528bd-125">Specifies the backup container type.</span></span>
<span data-ttu-id="528bd-126">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="528bd-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="528bd-127">AzureVM</span><span class="sxs-lookup"><span data-stu-id="528bd-127">AzureVM</span></span>
- <span data-ttu-id="528bd-128">Windows</span><span class="sxs-lookup"><span data-stu-id="528bd-128">Windows</span></span>
- <span data-ttu-id="528bd-129">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="528bd-129">AzureSQL</span></span>
- <span data-ttu-id="528bd-130">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="528bd-130">AzureStorage</span></span>
- <span data-ttu-id="528bd-131">AzureVMAppContainer</span><span class="sxs-lookup"><span data-stu-id="528bd-131">AzureVMAppContainer</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, Windows, AzureSQL, AzureStorage, AzureVMAppContainer

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="528bd-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="528bd-132">-DefaultProfile</span></span>

<span data-ttu-id="528bd-133">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="528bd-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="528bd-134">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="528bd-134">-FriendlyName</span></span>

<span data-ttu-id="528bd-135">Especifica o nome amigável do contêiner a obter.</span><span class="sxs-lookup"><span data-stu-id="528bd-135">Specifies the friendly name of the container to get.</span></span>

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

### <span data-ttu-id="528bd-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="528bd-136">-ResourceGroupName</span></span>

<span data-ttu-id="528bd-137">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="528bd-137">Specifies the name of the resource group.</span></span>
<span data-ttu-id="528bd-138">Este parâmetro é somente para máquinas virtuais do Azure.</span><span class="sxs-lookup"><span data-stu-id="528bd-138">This parameter is for Azure virtual machines only.</span></span>

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

### <span data-ttu-id="528bd-139">-Status</span><span class="sxs-lookup"><span data-stu-id="528bd-139">-Status</span></span>

<span data-ttu-id="528bd-140">Especifica o status de registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="528bd-140">Specifies the container registration status.</span></span>
<span data-ttu-id="528bd-141">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="528bd-141">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="528bd-142">Removido</span><span class="sxs-lookup"><span data-stu-id="528bd-142">Registered</span></span>

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

### <span data-ttu-id="528bd-143">-Cofreid</span><span class="sxs-lookup"><span data-stu-id="528bd-143">-VaultId</span></span>

<span data-ttu-id="528bd-144">ID do braço do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="528bd-144">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="528bd-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="528bd-145">CommonParameters</span></span>
<span data-ttu-id="528bd-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="528bd-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="528bd-147">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="528bd-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="528bd-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="528bd-148">INPUTS</span></span>

### <span data-ttu-id="528bd-149">System. String</span><span class="sxs-lookup"><span data-stu-id="528bd-149">System.String</span></span>

## <span data-ttu-id="528bd-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="528bd-150">OUTPUTS</span></span>

### <span data-ttu-id="528bd-151">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="528bd-151">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="528bd-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="528bd-152">NOTES</span></span>

## <span data-ttu-id="528bd-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="528bd-153">RELATED LINKS</span></span>

[<span data-ttu-id="528bd-154">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="528bd-154">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="528bd-155">Get-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="528bd-155">Get-AzRecoveryServicesBackupManagementServer</span></span>](./Get-AzRecoveryServicesBackupManagementServer.md)

[<span data-ttu-id="528bd-156">Cancelar registro-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="528bd-156">Unregister-AzRecoveryServicesBackupContainer</span></span>](./Unregister-AzRecoveryServicesBackupContainer.md)
