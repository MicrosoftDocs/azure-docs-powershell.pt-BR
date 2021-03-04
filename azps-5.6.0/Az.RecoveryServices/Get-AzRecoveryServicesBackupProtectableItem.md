---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectableItem.md
ms.openlocfilehash: 1d14a1559d62f00b4a513c6a25dad28b7816e2d1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890360"
---
# <span data-ttu-id="2b9da-101">Get-AzRecoveryServicesBackupProtectableItem</span><span class="sxs-lookup"><span data-stu-id="2b9da-101">Get-AzRecoveryServicesBackupProtectableItem</span></span>

## <span data-ttu-id="2b9da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b9da-102">SYNOPSIS</span></span>
<span data-ttu-id="2b9da-103">Este comando recuperará todos os itens protegidos em um determinado contêiner ou em todos os contêineres registrados.</span><span class="sxs-lookup"><span data-stu-id="2b9da-103">This command will retrieve all protectable items within a certain container or across all registered containers.</span></span> <span data-ttu-id="2b9da-104">Ele consistirá em todos os elementos da hierarquia do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2b9da-104">It will consist of all the elements of the hierarchy of the application.</span></span> <span data-ttu-id="2b9da-105">Retorna DBs e suas entidades de camada superior, como Instância, AvailabilityGroup etc.</span><span class="sxs-lookup"><span data-stu-id="2b9da-105">Returns DBs and their upper tier entities like Instance, AvailabilityGroup etc.</span></span>

## <span data-ttu-id="2b9da-106">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="2b9da-106">SYNTAX</span></span>

### <span data-ttu-id="2b9da-107">NoFilterParamSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="2b9da-107">NoFilterParamSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupProtectableItem [[-Container] <ContainerBase>] [-WorkloadType] <WorkloadType>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2b9da-108">FilterParamSet</span><span class="sxs-lookup"><span data-stu-id="2b9da-108">FilterParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectableItem [[-Container] <ContainerBase>] [-WorkloadType] <WorkloadType>
 [[-ItemType] <ProtectableItemType>] [-Name <String>] [-ServerName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2b9da-109">IdParamSet</span><span class="sxs-lookup"><span data-stu-id="2b9da-109">IdParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectableItem [-ParentID] <String> [[-ItemType] <ProtectableItemType>]
 [-Name <String>] [-ServerName <String>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2b9da-110">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="2b9da-110">DESCRIPTION</span></span>
<span data-ttu-id="2b9da-111">O cmdlet **Get-AzRecoveryServicesBackupProtectableItem** obtém a lista de itens protegidos em um contêiner e o status de proteção dos itens.</span><span class="sxs-lookup"><span data-stu-id="2b9da-111">The **Get-AzRecoveryServicesBackupProtectableItem** cmdlet gets the list of protectable items in a container and the protection status of the items.</span></span>
<span data-ttu-id="2b9da-112">Um contêiner que está registrado em um cofre dos Serviços de Recuperação do Azure pode ter um ou mais itens que podem ser protegidos.</span><span class="sxs-lookup"><span data-stu-id="2b9da-112">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>

## <span data-ttu-id="2b9da-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2b9da-113">EXAMPLES</span></span>

### <span data-ttu-id="2b9da-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2b9da-114">Example 1</span></span>
```
PS C:\> $Vault = Get-AzRecoveryServicesVault -Name "MyRecoveryVault"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVMAppContainer -Status Registered -VaultId $Vault.Id
PS C:\> $Item = Get-AzRecoveryServicesBackupProtectableItem -Container $Container -ItemType "SQLInstance" -WorkloadType "MSSQL" -VaultId $Vault.ID
```

<span data-ttu-id="2b9da-115">O primeiro comando obtém o contêiner do tipo MSSQL e o armazena na variável $Container.</span><span class="sxs-lookup"><span data-stu-id="2b9da-115">The first command gets the container of type MSSQL, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="2b9da-116">O segundo comando obtém o item protegido backup no $Container e o armazena na variável $Item backup.</span><span class="sxs-lookup"><span data-stu-id="2b9da-116">The second command gets the Backup protectable item in $Container, and then stores it in the $Item variable.</span></span>

## <span data-ttu-id="2b9da-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="2b9da-117">PARAMETERS</span></span>

### <span data-ttu-id="2b9da-118">-Container</span><span class="sxs-lookup"><span data-stu-id="2b9da-118">-Container</span></span>
<span data-ttu-id="2b9da-119">Contêiner onde o item reside</span><span class="sxs-lookup"><span data-stu-id="2b9da-119">Container where the item resides</span></span>

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

### <span data-ttu-id="2b9da-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b9da-120">-DefaultProfile</span></span>
<span data-ttu-id="2b9da-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2b9da-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b9da-122">-ItemType</span><span class="sxs-lookup"><span data-stu-id="2b9da-122">-ItemType</span></span>
<span data-ttu-id="2b9da-123">Especifica o tipo de item protegido.</span><span class="sxs-lookup"><span data-stu-id="2b9da-123">Specifies the type of protectable item.</span></span> <span data-ttu-id="2b9da-124">Valores aplicáveis: (SQLDataBase, SQLInstance, SQLAvailabilityGroup).</span><span class="sxs-lookup"><span data-stu-id="2b9da-124">Applicable values: (SQLDataBase, SQLInstance, SQLAvailabilityGroup).</span></span>

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

### <span data-ttu-id="2b9da-125">-Name</span><span class="sxs-lookup"><span data-stu-id="2b9da-125">-Name</span></span>
<span data-ttu-id="2b9da-126">Especifica o nome do Database, Instance ou AvailabilityGroup.</span><span class="sxs-lookup"><span data-stu-id="2b9da-126">Specifies the name of the Database, Instance or AvailabilityGroup.</span></span>

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

### <span data-ttu-id="2b9da-127">-ParentID</span><span class="sxs-lookup"><span data-stu-id="2b9da-127">-ParentID</span></span>
<span data-ttu-id="2b9da-128">Especificou a ARM ID de uma Instância ou AG.</span><span class="sxs-lookup"><span data-stu-id="2b9da-128">Specified the ARM ID of an Instance or AG.</span></span>

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

### <span data-ttu-id="2b9da-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2b9da-129">-ServerName</span></span>
<span data-ttu-id="2b9da-130">Especifica o nome do servidor ao qual o item pertence.</span><span class="sxs-lookup"><span data-stu-id="2b9da-130">Specifies the name of the server to which the item belongs.</span></span>

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

### <span data-ttu-id="2b9da-131">-VaultId</span><span class="sxs-lookup"><span data-stu-id="2b9da-131">-VaultId</span></span>
<span data-ttu-id="2b9da-132">ARM ID do Cofre de Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="2b9da-132">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="2b9da-133">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="2b9da-133">-WorkloadType</span></span>
<span data-ttu-id="2b9da-134">Tipo de carga de trabalho do recurso.</span><span class="sxs-lookup"><span data-stu-id="2b9da-134">Workload type of the resource.</span></span> <span data-ttu-id="2b9da-135">Os valores atuais suportados são AzureVM, WindowsServer, AzureFiles, MSSQL</span><span class="sxs-lookup"><span data-stu-id="2b9da-135">The current supported values are  AzureVM, WindowsServer, AzureFiles, MSSQL</span></span>

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

### <span data-ttu-id="2b9da-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b9da-136">CommonParameters</span></span>
<span data-ttu-id="2b9da-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b9da-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b9da-138">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2b9da-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b9da-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2b9da-139">INPUTS</span></span>

### <span data-ttu-id="2b9da-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span><span class="sxs-lookup"><span data-stu-id="2b9da-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>
<span data-ttu-id="2b9da-141">System.String</span><span class="sxs-lookup"><span data-stu-id="2b9da-141">System.String</span></span>

## <span data-ttu-id="2b9da-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="2b9da-142">OUTPUTS</span></span>

### <span data-ttu-id="2b9da-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ProtectableItemBase</span><span class="sxs-lookup"><span data-stu-id="2b9da-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ProtectableItemBase</span></span>

## <span data-ttu-id="2b9da-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="2b9da-144">NOTES</span></span>

## <span data-ttu-id="2b9da-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2b9da-145">RELATED LINKS</span></span>
