---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/initialize-azrecoveryservicesbackupprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Initialize-AzRecoveryServicesBackupProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Initialize-AzRecoveryServicesBackupProtectableItem.md
ms.openlocfilehash: 0fd0473cccdf8fbef3d3bab941ab6b3ce7813a63
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772985"
---
# <span data-ttu-id="9bc00-101">Initialize-AzRecoveryServicesBackupProtectableItem</span><span class="sxs-lookup"><span data-stu-id="9bc00-101">Initialize-AzRecoveryServicesBackupProtectableItem</span></span>

## <span data-ttu-id="9bc00-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9bc00-102">SYNOPSIS</span></span>
<span data-ttu-id="9bc00-103">Esse comando dispara a descoberta de itens desprotegidos do tipo de carga de trabalho fornecido no contêiner fornecido.</span><span class="sxs-lookup"><span data-stu-id="9bc00-103">This command triggers the discovery of any unprotected items of the given workload type in the given container.</span></span> <span data-ttu-id="9bc00-104">Se o aplicativo de banco de usuários não for protegido automaticamente, use esse comando para descobrir novos bancos de usuários sempre que eles forem adicionados e continuar a protegê-los.</span><span class="sxs-lookup"><span data-stu-id="9bc00-104">If the DB application is not auto-protected use this command to discover new DBs whenever they are added and proceed to protect them.</span></span>

## <span data-ttu-id="9bc00-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9bc00-105">SYNTAX</span></span>

```
Initialize-AzRecoveryServicesBackupProtectableItem [-Container] <ContainerBase> [-WorkloadType] <WorkloadType>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9bc00-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9bc00-106">DESCRIPTION</span></span>
<span data-ttu-id="9bc00-107">o cmdlet consulta as cargas de trabalho específicas dentro de um contêiner.</span><span class="sxs-lookup"><span data-stu-id="9bc00-107">the cmdlet enquires for specific workloads within a container.</span></span> <span data-ttu-id="9bc00-108">Isso aciona uma operação que cria itens que protegem.</span><span class="sxs-lookup"><span data-stu-id="9bc00-108">This triggers an operation which creates protectable items.</span></span>

## <span data-ttu-id="9bc00-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9bc00-109">EXAMPLES</span></span>

### <span data-ttu-id="9bc00-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9bc00-110">Example 1</span></span>
```
PS C:\> Initialize-AzRecoveryServicesProtectableItem -Container $Container –WorkloadType “MSSQL”
```

<span data-ttu-id="9bc00-111">O cmdlet executa uma operação de descoberta para novos itens que protegem.</span><span class="sxs-lookup"><span data-stu-id="9bc00-111">The cmdlet executes a discovery operation for new protectable items.</span></span>

## <span data-ttu-id="9bc00-112">OS</span><span class="sxs-lookup"><span data-stu-id="9bc00-112">PARAMETERS</span></span>

### <span data-ttu-id="9bc00-113">-Contêiner</span><span class="sxs-lookup"><span data-stu-id="9bc00-113">-Container</span></span>
<span data-ttu-id="9bc00-114">Contêiner em que o item reside</span><span class="sxs-lookup"><span data-stu-id="9bc00-114">Container where the item resides</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9bc00-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bc00-115">-DefaultProfile</span></span>
<span data-ttu-id="9bc00-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9bc00-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9bc00-117">-Cofreid</span><span class="sxs-lookup"><span data-stu-id="9bc00-117">-VaultId</span></span>
<span data-ttu-id="9bc00-118">ID do braço do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="9bc00-118">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="9bc00-119">-Workloadtype</span><span class="sxs-lookup"><span data-stu-id="9bc00-119">-WorkloadType</span></span>
<span data-ttu-id="9bc00-120">Tipo de carga de trabalho do recurso (por exemplo: AzureVM, WindowsServer, AzureFiles, MSSQL).</span><span class="sxs-lookup"><span data-stu-id="9bc00-120">Workload type of the resource (for example: AzureVM, WindowsServer, AzureFiles, MSSQL).</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bc00-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bc00-121">CommonParameters</span></span>
<span data-ttu-id="9bc00-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bc00-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bc00-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9bc00-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bc00-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9bc00-124">INPUTS</span></span>

### <span data-ttu-id="9bc00-125">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="9bc00-125">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>
<span data-ttu-id="9bc00-126">System. String</span><span class="sxs-lookup"><span data-stu-id="9bc00-126">System.String</span></span>

## <span data-ttu-id="9bc00-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9bc00-127">OUTPUTS</span></span>

### <span data-ttu-id="9bc00-128">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. dobase</span><span class="sxs-lookup"><span data-stu-id="9bc00-128">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="9bc00-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9bc00-129">NOTES</span></span>

## <span data-ttu-id="9bc00-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9bc00-130">RELATED LINKS</span></span>