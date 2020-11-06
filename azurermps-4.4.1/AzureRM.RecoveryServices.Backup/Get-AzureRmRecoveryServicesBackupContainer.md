---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 1097FF29-1C23-4960-930C-5C1227419359
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupContainer.md
ms.openlocfilehash: e6b0633b43bc93c516c9c5b6f4872ecbd6d68520
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610477"
---
# <span data-ttu-id="07954-101">Get-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="07954-101">Get-AzureRmRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="07954-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="07954-102">SYNOPSIS</span></span>
<span data-ttu-id="07954-103">Obtém contêineres de backup.</span><span class="sxs-lookup"><span data-stu-id="07954-103">Gets Backup containers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07954-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="07954-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupContainer [-ContainerType] <ContainerType> [[-BackupManagementType] <String>]
 [[-Name] <String>] [[-FriendlyName] <String>] [[-ResourceGroupName] <String>]
 [[-Status] <ContainerRegistrationStatus>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07954-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="07954-105">DESCRIPTION</span></span>
<span data-ttu-id="07954-106">O cmdlet **Get-AzureRmRecoveryServicesBackupContainer** Obtém um contêiner de backup.</span><span class="sxs-lookup"><span data-stu-id="07954-106">The **Get-AzureRmRecoveryServicesBackupContainer** cmdlet gets a backup container.</span></span>
<span data-ttu-id="07954-107">Um contêiner de backup encapsula fontes de dados que são modelled como itens de backup.</span><span class="sxs-lookup"><span data-stu-id="07954-107">A Backup container encapsulates data sources that are modelled as backup items.</span></span>

<span data-ttu-id="07954-108">Defina o contexto do cofre usando o cmdlet Set-AzureRmRecoveryServicesVaultContext antes de usar o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="07954-108">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="07954-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="07954-109">EXAMPLES</span></span>

### <span data-ttu-id="07954-110">Exemplo 1: obter um contêiner específico</span><span class="sxs-lookup"><span data-stu-id="07954-110">Example 1: Get a specific container</span></span>
```
PS C:\>Get-AzureRmRecoveryServicesContainer -ContainerType "AzureVM" -Status "Registered" -Name "V2VM";
```

<span data-ttu-id="07954-111">Esse comando obtém o contêiner chamado V2VM do tipo AzureVM.</span><span class="sxs-lookup"><span data-stu-id="07954-111">This command gets the container named V2VM of type AzureVM.</span></span>

### <span data-ttu-id="07954-112">Exemplo 2: obter todos os contêineres de um tipo específico</span><span class="sxs-lookup"><span data-stu-id="07954-112">Example 2: Get all containers of a specific type</span></span>
```
PS C:\>Get-AzureRmRecoveryServicesBackupContainer -ContainerType Windows -BackupManagementType MARS
```

<span data-ttu-id="07954-113">Esse comando obtém todos os contêineres do Windows protegidos pelo agente de backup do Azure.</span><span class="sxs-lookup"><span data-stu-id="07954-113">This command gets all Windows containers that are protected by Azure Backup agent.</span></span>
<span data-ttu-id="07954-114">O parâmetro *BackupManagementType* é necessário apenas para contêineres do Windows.</span><span class="sxs-lookup"><span data-stu-id="07954-114">The *BackupManagementType* parameter is only required for Windows containers.</span></span>

## <span data-ttu-id="07954-115">OS</span><span class="sxs-lookup"><span data-stu-id="07954-115">PARAMETERS</span></span>

### <span data-ttu-id="07954-116">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="07954-116">-BackupManagementType</span></span>
<span data-ttu-id="07954-117">Especifica o tipo de gerenciamento de backup.</span><span class="sxs-lookup"><span data-stu-id="07954-117">Specifies the backup management type.</span></span>
<span data-ttu-id="07954-118">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="07954-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="07954-119">AzureVM</span><span class="sxs-lookup"><span data-stu-id="07954-119">AzureVM</span></span>
- <span data-ttu-id="07954-120">Marte</span><span class="sxs-lookup"><span data-stu-id="07954-120">MARS</span></span>
- <span data-ttu-id="07954-121">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="07954-121">AzureSQL</span></span>

<span data-ttu-id="07954-122">Esse parâmetro é usado para diferenciar máquinas Windows que tenham o backup usando o agente MARS ou outros mecanismos de backup.</span><span class="sxs-lookup"><span data-stu-id="07954-122">This parameter is used to differentiate Windows machines that are backed up using MARS agent or other backup engines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, MARS, AzureSQL

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07954-123">-ContainerType</span><span class="sxs-lookup"><span data-stu-id="07954-123">-ContainerType</span></span>
<span data-ttu-id="07954-124">Especifica o tipo de contêiner de backup.</span><span class="sxs-lookup"><span data-stu-id="07954-124">Specifies the backup container type.</span></span>
<span data-ttu-id="07954-125">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="07954-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="07954-126">AzureVM</span><span class="sxs-lookup"><span data-stu-id="07954-126">AzureVM</span></span> 
- <span data-ttu-id="07954-127">Windows</span><span class="sxs-lookup"><span data-stu-id="07954-127">Windows</span></span>
- <span data-ttu-id="07954-128">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="07954-128">AzureSQL</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, Windows, AzureSQL

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07954-129">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="07954-129">-FriendlyName</span></span>
<span data-ttu-id="07954-130">Especifica o nome amigável do contêiner a obter.</span><span class="sxs-lookup"><span data-stu-id="07954-130">Specifies the friendly name of the container to get.</span></span>

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

### <span data-ttu-id="07954-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="07954-131">-Name</span></span>
<span data-ttu-id="07954-132">Especifica o nome do contêiner a obter.</span><span class="sxs-lookup"><span data-stu-id="07954-132">Specifies the name of the container to get.</span></span>

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

### <span data-ttu-id="07954-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07954-133">-ResourceGroupName</span></span>
<span data-ttu-id="07954-134">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="07954-134">Specifies the name of the resource group.</span></span>
<span data-ttu-id="07954-135">Este parâmetro é somente para máquinas virtuais do Azure.</span><span class="sxs-lookup"><span data-stu-id="07954-135">This parameter is for Azure virtual machines only.</span></span>

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

### <span data-ttu-id="07954-136">-Status</span><span class="sxs-lookup"><span data-stu-id="07954-136">-Status</span></span>
<span data-ttu-id="07954-137">Especifica o status de registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="07954-137">Specifies the container registration status.</span></span>
<span data-ttu-id="07954-138">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="07954-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="07954-139">Removido</span><span class="sxs-lookup"><span data-stu-id="07954-139">Registered</span></span>

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

### <span data-ttu-id="07954-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07954-140">-DefaultProfile</span></span>
<span data-ttu-id="07954-141">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="07954-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07954-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07954-142">CommonParameters</span></span>
<span data-ttu-id="07954-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07954-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07954-144">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07954-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07954-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="07954-145">INPUTS</span></span>

## <span data-ttu-id="07954-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="07954-146">OUTPUTS</span></span>

### <span data-ttu-id="07954-147">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="07954-147">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

### <span data-ttu-id="07954-148">System. Collections. Generic. IList ' 1 [Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. ContainerBase]</span><span class="sxs-lookup"><span data-stu-id="07954-148">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase]</span></span>

## <span data-ttu-id="07954-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="07954-149">NOTES</span></span>

## <span data-ttu-id="07954-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="07954-150">RELATED LINKS</span></span>

[<span data-ttu-id="07954-151">Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="07954-151">Get-AzureRmRecoveryServicesBackupItem</span></span>](./Get-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="07954-152">Get-AzureRmRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="07954-152">Get-AzureRmRecoveryServicesBackupManagementServer</span></span>](./Get-AzureRmRecoveryServicesBackupManagementServer.md)

[<span data-ttu-id="07954-153">Cancelar registro-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="07954-153">Unregister-AzureRmRecoveryServicesBackupContainer</span></span>](./Unregister-AzureRmRecoveryServicesBackupContainer.md)


