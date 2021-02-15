---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectableItem.md
ms.openlocfilehash: 580f5fd7dc85857bff7257847806bb15dc646ad3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114561"
---
# <span data-ttu-id="09b37-101">Get-AzRecoveryServicesBackupProtectableItem</span><span class="sxs-lookup"><span data-stu-id="09b37-101">Get-AzRecoveryServicesBackupProtectableItem</span></span>

## <span data-ttu-id="09b37-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="09b37-102">SYNOPSIS</span></span>
<span data-ttu-id="09b37-103">Esse comando recuperará todos os itens protegidos dentro de um determinado contêiner ou em todos os contêineres registrados.</span><span class="sxs-lookup"><span data-stu-id="09b37-103">This command will retrieve all protectable items within a certain container or across all registered containers.</span></span> <span data-ttu-id="09b37-104">Ela consistirá em todos os elementos da hierarquia do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="09b37-104">It will consist of all the elements of the hierarchy of the application.</span></span> <span data-ttu-id="09b37-105">Retorna DBs e suas entidades de nível superior, como Instância, Grupo de Disponibilidade etc.</span><span class="sxs-lookup"><span data-stu-id="09b37-105">Returns DBs and their upper tier entities like Instance, AvailabilityGroup etc.</span></span>

## <span data-ttu-id="09b37-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="09b37-106">SYNTAX</span></span>

### <span data-ttu-id="09b37-107">NoFilterParamSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="09b37-107">NoFilterParamSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupProtectableItem [[-Container] <ContainerBase>] [-WorkloadType] <WorkloadType>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09b37-108">FilterParamSet</span><span class="sxs-lookup"><span data-stu-id="09b37-108">FilterParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectableItem [[-Container] <ContainerBase>] [-WorkloadType] <WorkloadType>
 [[-ItemType] <ProtectableItemType>] [-Name <String>] [-ServerName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09b37-109">IdParamSet</span><span class="sxs-lookup"><span data-stu-id="09b37-109">IdParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectableItem [-ParentID] <String> [[-ItemType] <ProtectableItemType>]
 [-Name <String>] [-ServerName <String>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="09b37-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="09b37-110">DESCRIPTION</span></span>
<span data-ttu-id="09b37-111">O cmdlet **Get-AzRecoveryServicesBackupProtectableItem** obtém a lista de itens protegidos em um contêiner e o status de proteção dos itens.</span><span class="sxs-lookup"><span data-stu-id="09b37-111">The **Get-AzRecoveryServicesBackupProtectableItem** cmdlet gets the list of protectable items in a container and the protection status of the items.</span></span>
<span data-ttu-id="09b37-112">Um contêiner registrado em um cofre dos Serviços de Recuperação do Azure pode ter um ou mais itens que podem ser protegidos.</span><span class="sxs-lookup"><span data-stu-id="09b37-112">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>

## <span data-ttu-id="09b37-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="09b37-113">EXAMPLES</span></span>

### <span data-ttu-id="09b37-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="09b37-114">Example 1</span></span>
```
PS C:\> $Vault = Get-AzRecoveryServicesVault -Name "MyRecoveryVault"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVMAppContainer -Status Registered -VaultId $Vault.Id
PS C:\> $Item = Get-AzRecoveryServicesBackupProtectableItem -Container $Container -ItemType "SQLInstance" -WorkloadType "MSSQL" -VaultId $Vault.ID
```

<span data-ttu-id="09b37-115">O primeiro comando obtém o contêiner do tipo MSSQL e o armazena na variável $Container dados.</span><span class="sxs-lookup"><span data-stu-id="09b37-115">The first command gets the container of type MSSQL, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="09b37-116">O segundo comando obtém o item protegido $Container backup e, em seguida, o armazena na variável $Item dados.</span><span class="sxs-lookup"><span data-stu-id="09b37-116">The second command gets the Backup protectable item in $Container, and then stores it in the $Item variable.</span></span>

## <span data-ttu-id="09b37-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="09b37-117">PARAMETERS</span></span>

### <span data-ttu-id="09b37-118">-Contêiner</span><span class="sxs-lookup"><span data-stu-id="09b37-118">-Container</span></span>
<span data-ttu-id="09b37-119">Contêiner onde o item reside</span><span class="sxs-lookup"><span data-stu-id="09b37-119">Container where the item resides</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase
Parameter Sets: NoFilterParamSet, FilterParamSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09b37-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09b37-120">-DefaultProfile</span></span>
<span data-ttu-id="09b37-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="09b37-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09b37-122">-ItemType</span><span class="sxs-lookup"><span data-stu-id="09b37-122">-ItemType</span></span>
<span data-ttu-id="09b37-123">Especifica o tipo de item protegido.</span><span class="sxs-lookup"><span data-stu-id="09b37-123">Specifies the type of protectable item.</span></span> <span data-ttu-id="09b37-124">Valores aplicáveis: (SQLDataBase, SQLInstance, SQLAvailabilityGroup).</span><span class="sxs-lookup"><span data-stu-id="09b37-124">Applicable values: (SQLDataBase, SQLInstance, SQLAvailabilityGroup).</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ProtectableItemType
Parameter Sets: FilterParamSet, IdParamSet
Aliases:
Accepted values: SQLDataBase, SQLInstance, SQLAvailabilityGroup

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09b37-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="09b37-125">-Name</span></span>
<span data-ttu-id="09b37-126">Especifica o nome do Banco de Dados, Instância ou Grupo de Disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="09b37-126">Specifies the name of the Database, Instance or AvailabilityGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: FilterParamSet, IdParamSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09b37-127">-ParentID</span><span class="sxs-lookup"><span data-stu-id="09b37-127">-ParentID</span></span>
<span data-ttu-id="09b37-128">Especificou a ID arm de uma Instância ou AG.</span><span class="sxs-lookup"><span data-stu-id="09b37-128">Specified the ARM ID of an Instance or AG.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09b37-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="09b37-129">-ServerName</span></span>
<span data-ttu-id="09b37-130">Especifica o nome do servidor ao qual o item pertence.</span><span class="sxs-lookup"><span data-stu-id="09b37-130">Specifies the name of the server to which the item belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: FilterParamSet, IdParamSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09b37-131">-VaultId</span><span class="sxs-lookup"><span data-stu-id="09b37-131">-VaultId</span></span>
<span data-ttu-id="09b37-132">ID arm do Cofre de Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="09b37-132">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="09b37-133">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="09b37-133">-WorkloadType</span></span>
<span data-ttu-id="09b37-134">Tipo de carga de trabalho do recurso.</span><span class="sxs-lookup"><span data-stu-id="09b37-134">Workload type of the resource.</span></span> <span data-ttu-id="09b37-135">Os valores atuais com suporte são AzureVM, WindowsServer, AzureFiles, MSSQL</span><span class="sxs-lookup"><span data-stu-id="09b37-135">The current supported values are  AzureVM, WindowsServer, AzureFiles, MSSQL</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: NoFilterParamSet, FilterParamSet
Aliases:
Accepted values: AzureVM, WindowsServer, AzureFiles, MSSQL

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09b37-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09b37-136">CommonParameters</span></span>
<span data-ttu-id="09b37-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09b37-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09b37-138">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="09b37-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09b37-139">Entradas</span><span class="sxs-lookup"><span data-stu-id="09b37-139">INPUTS</span></span>

### <span data-ttu-id="09b37-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span><span class="sxs-lookup"><span data-stu-id="09b37-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>
<span data-ttu-id="09b37-141">System.String</span><span class="sxs-lookup"><span data-stu-id="09b37-141">System.String</span></span>

## <span data-ttu-id="09b37-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="09b37-142">OUTPUTS</span></span>

### <span data-ttu-id="09b37-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ProtectableItemBase</span><span class="sxs-lookup"><span data-stu-id="09b37-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ProtectableItemBase</span></span>

## <span data-ttu-id="09b37-144">Notas</span><span class="sxs-lookup"><span data-stu-id="09b37-144">NOTES</span></span>

## <span data-ttu-id="09b37-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="09b37-145">RELATED LINKS</span></span>
