---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 1097FF29-1C23-4960-930C-5C1227419359
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupContainer.md
ms.openlocfilehash: c47c3e51d970302281af5a7ae3a6175f4af79739
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609759"
---
# <span data-ttu-id="b55af-101">Get-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="b55af-101">Get-AzureRmRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="b55af-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b55af-102">SYNOPSIS</span></span>
<span data-ttu-id="b55af-103">Obtém contêineres de backup.</span><span class="sxs-lookup"><span data-stu-id="b55af-103">Gets Backup containers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b55af-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b55af-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupContainer [-ContainerType] <ContainerType> [[-BackupManagementType] <String>]
 [[-Name] <String>] [[-FriendlyName] <String>] [[-ResourceGroupName] <String>]
 [[-Status] <ContainerRegistrationStatus>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b55af-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b55af-105">DESCRIPTION</span></span>
<span data-ttu-id="b55af-106">O cmdlet **Get-AzureRmRecoveryServicesBackupContainer** Obtém um contêiner de backup.</span><span class="sxs-lookup"><span data-stu-id="b55af-106">The **Get-AzureRmRecoveryServicesBackupContainer** cmdlet gets a backup container.</span></span>
<span data-ttu-id="b55af-107">Um contêiner de backup encapsula fontes de dados que são modelled como itens de backup.</span><span class="sxs-lookup"><span data-stu-id="b55af-107">A Backup container encapsulates data sources that are modelled as backup items.</span></span>
<span data-ttu-id="b55af-108">Defina o contexto do cofre usando o cmdlet Set-AzureRmRecoveryServicesVaultContext antes de usar o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="b55af-108">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="b55af-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b55af-109">EXAMPLES</span></span>

### <span data-ttu-id="b55af-110">Exemplo 1: obter um contêiner específico</span><span class="sxs-lookup"><span data-stu-id="b55af-110">Example 1: Get a specific container</span></span>
```
PS C:\>Get-AzureRmRecoveryServicesContainer -ContainerType "AzureVM" -Status "Registered" -Name "V2VM";
```

<span data-ttu-id="b55af-111">Esse comando obtém o contêiner chamado V2VM do tipo AzureVM.</span><span class="sxs-lookup"><span data-stu-id="b55af-111">This command gets the container named V2VM of type AzureVM.</span></span>

### <span data-ttu-id="b55af-112">Exemplo 2: obter todos os contêineres de um tipo específico</span><span class="sxs-lookup"><span data-stu-id="b55af-112">Example 2: Get all containers of a specific type</span></span>
```
PS C:\>Get-AzureRmRecoveryServicesBackupContainer -ContainerType Windows -BackupManagementType MARS
```

<span data-ttu-id="b55af-113">Esse comando obtém todos os contêineres do Windows protegidos pelo agente de backup do Azure.</span><span class="sxs-lookup"><span data-stu-id="b55af-113">This command gets all Windows containers that are protected by Azure Backup agent.</span></span>
<span data-ttu-id="b55af-114">O parâmetro *BackupManagementType* é necessário apenas para contêineres do Windows.</span><span class="sxs-lookup"><span data-stu-id="b55af-114">The *BackupManagementType* parameter is only required for Windows containers.</span></span>

## <span data-ttu-id="b55af-115">OS</span><span class="sxs-lookup"><span data-stu-id="b55af-115">PARAMETERS</span></span>

### <span data-ttu-id="b55af-116">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="b55af-116">-BackupManagementType</span></span>
<span data-ttu-id="b55af-117">Especifica o tipo de gerenciamento de backup.</span><span class="sxs-lookup"><span data-stu-id="b55af-117">Specifies the backup management type.</span></span>
<span data-ttu-id="b55af-118">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="b55af-118">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b55af-119">AzureVM</span><span class="sxs-lookup"><span data-stu-id="b55af-119">AzureVM</span></span>
- <span data-ttu-id="b55af-120">Marte</span><span class="sxs-lookup"><span data-stu-id="b55af-120">MARS</span></span>
- <span data-ttu-id="b55af-121">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="b55af-121">AzureSQL</span></span>
- <span data-ttu-id="b55af-122">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="b55af-122">AzureStorage</span></span>

<span data-ttu-id="b55af-123">Esse parâmetro é usado para diferenciar máquinas Windows que tenham o backup usando o agente MARS ou outros mecanismos de backup.</span><span class="sxs-lookup"><span data-stu-id="b55af-123">This parameter is used to differentiate Windows machines that are backed up using MARS agent or other backup engines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, AzureSQL, AzureStorage

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b55af-124">-ContainerType</span><span class="sxs-lookup"><span data-stu-id="b55af-124">-ContainerType</span></span>
<span data-ttu-id="b55af-125">Especifica o tipo de contêiner de backup.</span><span class="sxs-lookup"><span data-stu-id="b55af-125">Specifies the backup container type.</span></span>
<span data-ttu-id="b55af-126">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="b55af-126">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b55af-127">AzureVM</span><span class="sxs-lookup"><span data-stu-id="b55af-127">AzureVM</span></span> 
- <span data-ttu-id="b55af-128">Windows</span><span class="sxs-lookup"><span data-stu-id="b55af-128">Windows</span></span>
- <span data-ttu-id="b55af-129">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="b55af-129">AzureSQL</span></span>
- <span data-ttu-id="b55af-130">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="b55af-130">AzureStorage</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, Windows, AzureSQL, AzureStorage

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b55af-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b55af-131">-DefaultProfile</span></span>
<span data-ttu-id="b55af-132">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b55af-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b55af-133">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="b55af-133">-FriendlyName</span></span>
<span data-ttu-id="b55af-134">Especifica o nome amigável do contêiner a obter.</span><span class="sxs-lookup"><span data-stu-id="b55af-134">Specifies the friendly name of the container to get.</span></span>

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

### <span data-ttu-id="b55af-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="b55af-135">-Name</span></span>
<span data-ttu-id="b55af-136">Especifica o nome do contêiner a obter.</span><span class="sxs-lookup"><span data-stu-id="b55af-136">Specifies the name of the container to get.</span></span>

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

### <span data-ttu-id="b55af-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b55af-137">-ResourceGroupName</span></span>
<span data-ttu-id="b55af-138">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b55af-138">Specifies the name of the resource group.</span></span>
<span data-ttu-id="b55af-139">Este parâmetro é somente para máquinas virtuais do Azure.</span><span class="sxs-lookup"><span data-stu-id="b55af-139">This parameter is for Azure virtual machines only.</span></span>

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

### <span data-ttu-id="b55af-140">-Status</span><span class="sxs-lookup"><span data-stu-id="b55af-140">-Status</span></span>
<span data-ttu-id="b55af-141">Especifica o status de registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="b55af-141">Specifies the container registration status.</span></span>
<span data-ttu-id="b55af-142">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="b55af-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b55af-143">Removido</span><span class="sxs-lookup"><span data-stu-id="b55af-143">Registered</span></span>

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

### <span data-ttu-id="b55af-144">-Cofreid</span><span class="sxs-lookup"><span data-stu-id="b55af-144">-VaultId</span></span>
<span data-ttu-id="b55af-145">ID do braço do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="b55af-145">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="b55af-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b55af-146">CommonParameters</span></span>
<span data-ttu-id="b55af-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b55af-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b55af-148">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b55af-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b55af-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b55af-149">INPUTS</span></span>

### <span data-ttu-id="b55af-150">System. String</span><span class="sxs-lookup"><span data-stu-id="b55af-150">System.String</span></span>
<span data-ttu-id="b55af-151">Parâmetros: Vaultid (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b55af-151">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="b55af-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b55af-152">OUTPUTS</span></span>

### <span data-ttu-id="b55af-153">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="b55af-153">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="b55af-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b55af-154">NOTES</span></span>

## <span data-ttu-id="b55af-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b55af-155">RELATED LINKS</span></span>

[<span data-ttu-id="b55af-156">Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="b55af-156">Get-AzureRmRecoveryServicesBackupItem</span></span>](./Get-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="b55af-157">Get-AzureRmRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="b55af-157">Get-AzureRmRecoveryServicesBackupManagementServer</span></span>](./Get-AzureRmRecoveryServicesBackupManagementServer.md)

[<span data-ttu-id="b55af-158">Cancelar registro-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="b55af-158">Unregister-AzureRmRecoveryServicesBackupContainer</span></span>](./Unregister-AzureRmRecoveryServicesBackupContainer.md)


