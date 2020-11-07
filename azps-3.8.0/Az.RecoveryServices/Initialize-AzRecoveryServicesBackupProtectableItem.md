---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/initialize-azrecoveryservicesbackupprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Initialize-AzRecoveryServicesBackupProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Initialize-AzRecoveryServicesBackupProtectableItem.md
ms.openlocfilehash: 8bc2286cf6df736ee54390447e83f0337c031001
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944708"
---
# <span data-ttu-id="ee1c2-101">Initialize-AzRecoveryServicesBackupProtectableItem</span><span class="sxs-lookup"><span data-stu-id="ee1c2-101">Initialize-AzRecoveryServicesBackupProtectableItem</span></span>

## <span data-ttu-id="ee1c2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ee1c2-102">SYNOPSIS</span></span>
<span data-ttu-id="ee1c2-103">Esse comando dispara a descoberta de itens desprotegidos do tipo de carga de trabalho fornecido no contêiner fornecido.</span><span class="sxs-lookup"><span data-stu-id="ee1c2-103">This command triggers the discovery of any unprotected items of the given workload type in the given container.</span></span> <span data-ttu-id="ee1c2-104">Se o aplicativo de banco de usuários não for protegido automaticamente, use esse comando para descobrir novos bancos de usuários sempre que eles forem adicionados e continuar a protegê-los.</span><span class="sxs-lookup"><span data-stu-id="ee1c2-104">If the DB application is not auto-protected use this command to discover new DBs whenever they are added and proceed to protect them.</span></span>

## <span data-ttu-id="ee1c2-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ee1c2-105">SYNTAX</span></span>

```
Initialize-AzRecoveryServicesBackupProtectableItem [-Container] <ContainerBase> [-WorkloadType] <WorkloadType>
 [-PassThru] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ee1c2-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ee1c2-106">DESCRIPTION</span></span>
<span data-ttu-id="ee1c2-107">o cmdlet consulta as cargas de trabalho específicas dentro de um contêiner.</span><span class="sxs-lookup"><span data-stu-id="ee1c2-107">the cmdlet enquires for specific workloads within a container.</span></span> <span data-ttu-id="ee1c2-108">Isso aciona uma operação que cria itens que protegem.</span><span class="sxs-lookup"><span data-stu-id="ee1c2-108">This triggers an operation which creates protectable items.</span></span>

## <span data-ttu-id="ee1c2-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ee1c2-109">EXAMPLES</span></span>

### <span data-ttu-id="ee1c2-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ee1c2-110">Example 1</span></span>
```
PS C:\> Initialize-AzRecoveryServicesProtectableItem -Container $Container -WorkloadType "MSSQL"
```

<span data-ttu-id="ee1c2-111">O cmdlet executa uma operação de descoberta para novos itens que protegem.</span><span class="sxs-lookup"><span data-stu-id="ee1c2-111">The cmdlet executes a discovery operation for new protectable items.</span></span>

## <span data-ttu-id="ee1c2-112">OS</span><span class="sxs-lookup"><span data-stu-id="ee1c2-112">PARAMETERS</span></span>

### <span data-ttu-id="ee1c2-113">-Contêiner</span><span class="sxs-lookup"><span data-stu-id="ee1c2-113">-Container</span></span>
<span data-ttu-id="ee1c2-114">Contêiner em que o item reside</span><span class="sxs-lookup"><span data-stu-id="ee1c2-114">Container where the item resides</span></span>

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

### <span data-ttu-id="ee1c2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee1c2-115">-DefaultProfile</span></span>
<span data-ttu-id="ee1c2-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ee1c2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee1c2-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ee1c2-117">-PassThru</span></span>
<span data-ttu-id="ee1c2-118">Retorne o contêiner a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="ee1c2-118">Return the container to be deleted.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee1c2-119">-Cofreid</span><span class="sxs-lookup"><span data-stu-id="ee1c2-119">-VaultId</span></span>
<span data-ttu-id="ee1c2-120">ID do braço do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="ee1c2-120">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="ee1c2-121">-Workloadtype</span><span class="sxs-lookup"><span data-stu-id="ee1c2-121">-WorkloadType</span></span>
<span data-ttu-id="ee1c2-122">Tipo de carga de trabalho do recurso (por exemplo: AzureVM, WindowsServer, AzureFiles, MSSQL).</span><span class="sxs-lookup"><span data-stu-id="ee1c2-122">Workload type of the resource (for example: AzureVM, WindowsServer, AzureFiles, MSSQL).</span></span>

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

### <span data-ttu-id="ee1c2-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ee1c2-123">-Confirm</span></span>
<span data-ttu-id="ee1c2-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee1c2-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee1c2-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee1c2-125">-WhatIf</span></span>
<span data-ttu-id="ee1c2-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ee1c2-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ee1c2-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ee1c2-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee1c2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee1c2-128">CommonParameters</span></span>
<span data-ttu-id="ee1c2-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee1c2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee1c2-130">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ee1c2-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee1c2-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ee1c2-131">INPUTS</span></span>

### <span data-ttu-id="ee1c2-132">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="ee1c2-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>
<span data-ttu-id="ee1c2-133">System. String</span><span class="sxs-lookup"><span data-stu-id="ee1c2-133">System.String</span></span>

## <span data-ttu-id="ee1c2-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ee1c2-134">OUTPUTS</span></span>

### <span data-ttu-id="ee1c2-135">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. dobase</span><span class="sxs-lookup"><span data-stu-id="ee1c2-135">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="ee1c2-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ee1c2-136">NOTES</span></span>

## <span data-ttu-id="ee1c2-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ee1c2-137">RELATED LINKS</span></span>
