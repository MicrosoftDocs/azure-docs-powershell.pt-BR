---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 1097FF29-1C23-4960-930C-5C1227419359
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupContainer.md
ms.openlocfilehash: 0fb1df2d72259c6c0f427a9a66f4cf271cc0cbfa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889422"
---
# <span data-ttu-id="744a5-101">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="744a5-101">Get-AzRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="744a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="744a5-102">SYNOPSIS</span></span>

<span data-ttu-id="744a5-103">Obtém contêineres de backup.</span><span class="sxs-lookup"><span data-stu-id="744a5-103">Gets Backup containers.</span></span>

## <span data-ttu-id="744a5-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="744a5-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupContainer [-ContainerType] <ContainerType> [[-BackupManagementType] <String>]
 [[-FriendlyName] <String>] [[-ResourceGroupName] <String>] [[-Status] <ContainerRegistrationStatus>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="744a5-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="744a5-105">DESCRIPTION</span></span>

<span data-ttu-id="744a5-106">O cmdlet **Get-AzRecoveryServicesBackupContainer** obtém um contêiner de backup.</span><span class="sxs-lookup"><span data-stu-id="744a5-106">The **Get-AzRecoveryServicesBackupContainer** cmdlet gets a backup container.</span></span> <span data-ttu-id="744a5-107">Um contêiner de backup encapsula fontes de dados que são modeladas como itens de backup.</span><span class="sxs-lookup"><span data-stu-id="744a5-107">A Backup container encapsulates data sources that are modelled as backup items.</span></span>
<span data-ttu-id="744a5-108">Para o tipo de contêiner "Azure VM", a saída lista todos os contêineres cujo nome corresponde exatamente ao que foi passado como o valor do parâmetro Friendly Name.</span><span class="sxs-lookup"><span data-stu-id="744a5-108">For Container type "Azure VM" , the output lists all the containers whose name exactly matches to the one passed  as the value for Friendly Name parameter.</span></span> <span data-ttu-id="744a5-109">Para outros tipos de contêiner, a saída fornece uma lista de contêineres com nome semelhante ao valor passado para o parâmetro Friendly name.</span><span class="sxs-lookup"><span data-stu-id="744a5-109">For other container types,  output gives a list of containers with name similar to the value passed for Friendly name parameter.</span></span>
<span data-ttu-id="744a5-110">De definir o contexto do cofre usando o parâmetro -VaultId.</span><span class="sxs-lookup"><span data-stu-id="744a5-110">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="744a5-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="744a5-111">EXAMPLES</span></span>

### <span data-ttu-id="744a5-112">Exemplo 1: Obter um contêiner específico</span><span class="sxs-lookup"><span data-stu-id="744a5-112">Example 1: Get a specific container</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupContainer -ContainerType "AzureVM" -Status "Registered" -FriendlyName "V2VM" -VaultId $vault.ID
```

<span data-ttu-id="744a5-113">Este comando obtém o contêiner chamado V2VM do tipo AzureVM.</span><span class="sxs-lookup"><span data-stu-id="744a5-113">This command gets the container named V2VM of type AzureVM.</span></span>

### <span data-ttu-id="744a5-114">Exemplo 2: Obter todos os contêineres de um tipo específico</span><span class="sxs-lookup"><span data-stu-id="744a5-114">Example 2: Get all containers of a specific type</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupContainer -ContainerType Windows -BackupManagementType MARS -VaultId $vault.ID
```

<span data-ttu-id="744a5-115">Esse comando obtém todos os contêineres do Windows protegidos pelo agente de Backup do Azure.</span><span class="sxs-lookup"><span data-stu-id="744a5-115">This command gets all Windows containers that are protected by Azure Backup agent.</span></span>
<span data-ttu-id="744a5-116">O **parâmetro BackupManagementType** só é necessário para contêineres do Windows.</span><span class="sxs-lookup"><span data-stu-id="744a5-116">The **BackupManagementType** parameter is only required for Windows containers.</span></span>

## <span data-ttu-id="744a5-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="744a5-117">PARAMETERS</span></span>

### <span data-ttu-id="744a5-118">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="744a5-118">-BackupManagementType</span></span>

<span data-ttu-id="744a5-119">A classe de recursos que está sendo protegida.</span><span class="sxs-lookup"><span data-stu-id="744a5-119">The class of resources being protected.</span></span> <span data-ttu-id="744a5-120">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="744a5-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="744a5-121">AzureVM</span><span class="sxs-lookup"><span data-stu-id="744a5-121">AzureVM</span></span>
- <span data-ttu-id="744a5-122">MARS</span><span class="sxs-lookup"><span data-stu-id="744a5-122">MARS</span></span>
- <span data-ttu-id="744a5-123">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="744a5-123">AzureWorkload</span></span>
- <span data-ttu-id="744a5-124">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="744a5-124">AzureStorage</span></span>

<span data-ttu-id="744a5-125">Esse parâmetro é usado para diferenciar computadores Windows que têm backup usando o agente MARS ou outros mecanismos de backup.</span><span class="sxs-lookup"><span data-stu-id="744a5-125">This parameter is used to differentiate Windows machines that are backed up using MARS agent or other backup engines.</span></span>

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

### <span data-ttu-id="744a5-126">-ContainerType</span><span class="sxs-lookup"><span data-stu-id="744a5-126">-ContainerType</span></span>

<span data-ttu-id="744a5-127">Especifica o tipo de contêiner de backup.</span><span class="sxs-lookup"><span data-stu-id="744a5-127">Specifies the backup container type.</span></span>
<span data-ttu-id="744a5-128">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="744a5-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="744a5-129">AzureVM</span><span class="sxs-lookup"><span data-stu-id="744a5-129">AzureVM</span></span>
- <span data-ttu-id="744a5-130">Windows</span><span class="sxs-lookup"><span data-stu-id="744a5-130">Windows</span></span>
- <span data-ttu-id="744a5-131">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="744a5-131">AzureStorage</span></span>
- <span data-ttu-id="744a5-132">AzureVMAppContainer</span><span class="sxs-lookup"><span data-stu-id="744a5-132">AzureVMAppContainer</span></span>

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

### <span data-ttu-id="744a5-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="744a5-133">-DefaultProfile</span></span>

<span data-ttu-id="744a5-134">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="744a5-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="744a5-135">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="744a5-135">-FriendlyName</span></span>

<span data-ttu-id="744a5-136">Especifica o nome amigável do contêiner a ser encontrado.</span><span class="sxs-lookup"><span data-stu-id="744a5-136">Specifies the friendly name of the container to get.</span></span>

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

### <span data-ttu-id="744a5-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="744a5-137">-ResourceGroupName</span></span>

<span data-ttu-id="744a5-138">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="744a5-138">Specifies the name of the resource group.</span></span>
<span data-ttu-id="744a5-139">Este parâmetro é apenas para máquinas virtuais do Azure.</span><span class="sxs-lookup"><span data-stu-id="744a5-139">This parameter is for Azure virtual machines only.</span></span>

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

### <span data-ttu-id="744a5-140">-Status</span><span class="sxs-lookup"><span data-stu-id="744a5-140">-Status</span></span>

<span data-ttu-id="744a5-141">Especifica o status de registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="744a5-141">Specifies the container registration status.</span></span>
<span data-ttu-id="744a5-142">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="744a5-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="744a5-143">Registrado</span><span class="sxs-lookup"><span data-stu-id="744a5-143">Registered</span></span>

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

### <span data-ttu-id="744a5-144">-VaultId</span><span class="sxs-lookup"><span data-stu-id="744a5-144">-VaultId</span></span>

<span data-ttu-id="744a5-145">ARM ID do Cofre de Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="744a5-145">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="744a5-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="744a5-146">CommonParameters</span></span>
<span data-ttu-id="744a5-147">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="744a5-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="744a5-148">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="744a5-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="744a5-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="744a5-149">INPUTS</span></span>

### <span data-ttu-id="744a5-150">System.String</span><span class="sxs-lookup"><span data-stu-id="744a5-150">System.String</span></span>

## <span data-ttu-id="744a5-151">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="744a5-151">OUTPUTS</span></span>

### <span data-ttu-id="744a5-152">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span><span class="sxs-lookup"><span data-stu-id="744a5-152">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="744a5-153">NOTES</span><span class="sxs-lookup"><span data-stu-id="744a5-153">NOTES</span></span>

## <span data-ttu-id="744a5-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="744a5-154">RELATED LINKS</span></span>

[<span data-ttu-id="744a5-155">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="744a5-155">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="744a5-156">Get-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="744a5-156">Get-AzRecoveryServicesBackupManagementServer</span></span>](./Get-AzRecoveryServicesBackupManagementServer.md)

[<span data-ttu-id="744a5-157">Unregister-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="744a5-157">Unregister-AzRecoveryServicesBackupContainer</span></span>](./Unregister-AzRecoveryServicesBackupContainer.md)
