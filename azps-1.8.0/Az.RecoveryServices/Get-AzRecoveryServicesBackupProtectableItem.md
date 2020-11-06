---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectableItem.md
ms.openlocfilehash: 03e990f36c8846ad1055d5d2f8873ead18536128
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599699"
---
# <span data-ttu-id="4ffc3-101">Get-AzRecoveryServicesBackupProtectableItem</span><span class="sxs-lookup"><span data-stu-id="4ffc3-101">Get-AzRecoveryServicesBackupProtectableItem</span></span>

## <span data-ttu-id="4ffc3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4ffc3-102">SYNOPSIS</span></span>
<span data-ttu-id="4ffc3-103">Esse comando recuperará todos os itens que protegem dentro de um determinado contêiner ou em todos os contêineres registrados.</span><span class="sxs-lookup"><span data-stu-id="4ffc3-103">This command will retrieve all protectable items within a certain container or across all registered containers.</span></span> <span data-ttu-id="4ffc3-104">Ele consistirá em todos os elementos da hierarquia do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4ffc3-104">It will consist of all the elements of the hierarchy of the application.</span></span> <span data-ttu-id="4ffc3-105">Retorna bancos de bancos e suas entidades de camada superior, como instância, Availabilitygroup, etc.</span><span class="sxs-lookup"><span data-stu-id="4ffc3-105">Returns DBs and their upper tier entities like Instance, AvailabilityGroup etc.</span></span>

## <span data-ttu-id="4ffc3-106">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4ffc3-106">SYNTAX</span></span>

### <span data-ttu-id="4ffc3-107">NoFilterParamSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="4ffc3-107">NoFilterParamSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupProtectableItem [[-Container] <ContainerBase>] [-WorkloadType] <WorkloadType>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4ffc3-108">FilterParamSet</span><span class="sxs-lookup"><span data-stu-id="4ffc3-108">FilterParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectableItem [[-Container] <ContainerBase>] [-WorkloadType] <WorkloadType>
 [[-ItemType] <ProtectableItemType>] [-Name <String>] [-ServerName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4ffc3-109">IdParamSet</span><span class="sxs-lookup"><span data-stu-id="4ffc3-109">IdParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectableItem [-ParentID] <String> [[-ItemType] <ProtectableItemType>]
 [-Name <String>] [-ServerName <String>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4ffc3-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4ffc3-110">DESCRIPTION</span></span>
<span data-ttu-id="4ffc3-111">O cmdlet **Get-AzRecoveryServicesBackupProtectableItem** Obtém os itens que protegem em um contêiner ou um valor no Azure backup e o status de proteção dos itens.</span><span class="sxs-lookup"><span data-stu-id="4ffc3-111">The **Get-AzRecoveryServicesBackupProtectableItem** cmdlet gets the protectable items in a container or a value in Azure Backup and the protection status of the items.</span></span>
<span data-ttu-id="4ffc3-112">Um contêiner que está registrado para um cofre de serviços de recuperação do Azure pode ter um ou mais itens que podem ser protegidos.</span><span class="sxs-lookup"><span data-stu-id="4ffc3-112">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>

## <span data-ttu-id="4ffc3-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4ffc3-113">EXAMPLES</span></span>

### <span data-ttu-id="4ffc3-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4ffc3-114">Example 1</span></span>
```
PS C:\>$Container = Get-AzRecoveryServicesBackupContainer -ContainerType MSSQL -Status Registered
PS C:\> $Item = Get-AzRecoveryServicesProtectableItem -Container $Container -ItemType "SQLDatabase" -VaultId $vault.ID
```

<span data-ttu-id="4ffc3-115">O primeiro comando obtém o contêiner do tipo MSSQL e, em seguida, armazena-o na variável $Container.</span><span class="sxs-lookup"><span data-stu-id="4ffc3-115">The first command gets the container of type MSSQL, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="4ffc3-116">O segundo comando obtém o item de backup no $Container e, em seguida, armazena-o na variável $Item.</span><span class="sxs-lookup"><span data-stu-id="4ffc3-116">The second command gets the Backup item in $Container, and then stores it in the $Item variable.</span></span>

## <span data-ttu-id="4ffc3-117">OS</span><span class="sxs-lookup"><span data-stu-id="4ffc3-117">PARAMETERS</span></span>

### <span data-ttu-id="4ffc3-118">-Contêiner</span><span class="sxs-lookup"><span data-stu-id="4ffc3-118">-Container</span></span>
<span data-ttu-id="4ffc3-119">Contêiner em que o item reside</span><span class="sxs-lookup"><span data-stu-id="4ffc3-119">Container where the item resides</span></span>

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

### <span data-ttu-id="4ffc3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ffc3-120">-DefaultProfile</span></span>
<span data-ttu-id="4ffc3-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4ffc3-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ffc3-122">-ItemType</span><span class="sxs-lookup"><span data-stu-id="4ffc3-122">-ItemType</span></span>
<span data-ttu-id="4ffc3-123">Especifica o tipo de item de proteção.</span><span class="sxs-lookup"><span data-stu-id="4ffc3-123">Specifies the type of protectable item.</span></span> <span data-ttu-id="4ffc3-124">Valores aplicáveis: (SQLDatabase, SQLInstance, sqlavailability myavailability).</span><span class="sxs-lookup"><span data-stu-id="4ffc3-124">Applicable values: (SQLDataBase, SQLInstance, SQLAvailabilityGroup).</span></span>

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

### <span data-ttu-id="4ffc3-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="4ffc3-125">-Name</span></span>
<span data-ttu-id="4ffc3-126">Especifica o nome do banco de dados, instância ou Availabilitygroup.</span><span class="sxs-lookup"><span data-stu-id="4ffc3-126">Specifies the name of the Database, Instance or AvailabilityGroup.</span></span>

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

### <span data-ttu-id="4ffc3-127">-ParentID</span><span class="sxs-lookup"><span data-stu-id="4ffc3-127">-ParentID</span></span>
<span data-ttu-id="4ffc3-128">Especificou a ID do ARM de uma instância ou AG.</span><span class="sxs-lookup"><span data-stu-id="4ffc3-128">Specified the ARM ID of an Instance or AG.</span></span>

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

### <span data-ttu-id="4ffc3-129">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="4ffc3-129">-ServerName</span></span>
<span data-ttu-id="4ffc3-130">Especifica o nome do servidor ao qual o item pertence.</span><span class="sxs-lookup"><span data-stu-id="4ffc3-130">Specifies the name of the server to which the item belongs.</span></span>

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

### <span data-ttu-id="4ffc3-131">-Cofreid</span><span class="sxs-lookup"><span data-stu-id="4ffc3-131">-VaultId</span></span>
<span data-ttu-id="4ffc3-132">ID do braço do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="4ffc3-132">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="4ffc3-133">-Workloadtype</span><span class="sxs-lookup"><span data-stu-id="4ffc3-133">-WorkloadType</span></span>
<span data-ttu-id="4ffc3-134">Tipo de carga de trabalho do recurso (por exemplo: AzureVM, WindowsServer, AzureFiles, MSSQL).</span><span class="sxs-lookup"><span data-stu-id="4ffc3-134">Workload type of the resource (for example: AzureVM, WindowsServer, AzureFiles, MSSQL).</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: NoFilterParamSet, FilterParamSet
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ffc3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ffc3-135">CommonParameters</span></span>
<span data-ttu-id="4ffc3-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ffc3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ffc3-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ffc3-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ffc3-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4ffc3-138">INPUTS</span></span>

### <span data-ttu-id="4ffc3-139">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="4ffc3-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>
<span data-ttu-id="4ffc3-140">System. String</span><span class="sxs-lookup"><span data-stu-id="4ffc3-140">System.String</span></span>

## <span data-ttu-id="4ffc3-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4ffc3-141">OUTPUTS</span></span>

### <span data-ttu-id="4ffc3-142">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. ProtectableItemBase</span><span class="sxs-lookup"><span data-stu-id="4ffc3-142">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ProtectableItemBase</span></span>

## <span data-ttu-id="4ffc3-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4ffc3-143">NOTES</span></span>

## <span data-ttu-id="4ffc3-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4ffc3-144">RELATED LINKS</span></span>