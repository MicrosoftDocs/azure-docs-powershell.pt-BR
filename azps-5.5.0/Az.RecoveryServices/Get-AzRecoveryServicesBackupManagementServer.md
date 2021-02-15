---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 4B7ACEC8-29BB-4791-8087-801300F246B4
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupmanagementserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupManagementServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupManagementServer.md
ms.openlocfilehash: 09d27926f489feea397c98a217840bb973e002ce
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114049"
---
# <span data-ttu-id="bb2bf-101">Get-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="bb2bf-101">Get-AzRecoveryServicesBackupManagementServer</span></span>

## <span data-ttu-id="bb2bf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bb2bf-102">SYNOPSIS</span></span>
<span data-ttu-id="bb2bf-103">Obtém servidores de gerenciamento de backup do SCDPM e do Azure.</span><span class="sxs-lookup"><span data-stu-id="bb2bf-103">Gets SCDPM and Azure Backup management servers.</span></span>

## <span data-ttu-id="bb2bf-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bb2bf-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupManagementServer [[-Name] <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb2bf-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="bb2bf-105">DESCRIPTION</span></span>
<span data-ttu-id="bb2bf-106">O cmdlet **Get-AzRecoveryServicesBackupManagementServer** obtém uma lista de servidores de gerenciamento de backup registrados em um cofre.</span><span class="sxs-lookup"><span data-stu-id="bb2bf-106">The **Get-AzRecoveryServicesBackupManagementServer** cmdlet gets a list of Backup management servers that are registered in a vault.</span></span>
<span data-ttu-id="bb2bf-107">Há dois tipos de servidores de gerenciamento de backup: o System Center Data Protection Manager (SCDPM) e os servidores de gerenciamento de backup do Azure.</span><span class="sxs-lookup"><span data-stu-id="bb2bf-107">There are two types of Backup management servers: System Center Data Protection Manager (SCDPM) and Azure Backup management servers.</span></span>
<span data-ttu-id="bb2bf-108">Os servidores de gerenciamento de backup são instalados separadamente para gerenciar a orquestão de backup.</span><span class="sxs-lookup"><span data-stu-id="bb2bf-108">Backup management servers are installed separately to manage Backup orchestration.</span></span>
<span data-ttu-id="bb2bf-109">De definir o contexto do cofre usando o Set-AzRecoveryServicesVaultContext cmdlet antes de usar o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="bb2bf-109">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="bb2bf-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="bb2bf-110">EXAMPLES</span></span>

### <span data-ttu-id="bb2bf-111">Exemplo 1: Obter todos os servidores de gerenciamento de backup</span><span class="sxs-lookup"><span data-stu-id="bb2bf-111">Example 1: Get all Backup management servers</span></span>
```
PS C:\>Get-AzRecoveryServicesBackupManagementServer
```

<span data-ttu-id="bb2bf-112">Esse comando registra todos os servidores de gerenciamento de backup com o cofre.</span><span class="sxs-lookup"><span data-stu-id="bb2bf-112">This command gets all Backup management servers registered with the vault.</span></span>

## <span data-ttu-id="bb2bf-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bb2bf-113">PARAMETERS</span></span>

### <span data-ttu-id="bb2bf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb2bf-114">-DefaultProfile</span></span>
<span data-ttu-id="bb2bf-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="bb2bf-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb2bf-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="bb2bf-116">-Name</span></span>
<span data-ttu-id="bb2bf-117">Especifica o nome do servidor de gerenciamento de backup para obter.</span><span class="sxs-lookup"><span data-stu-id="bb2bf-117">Specifies the name of the Backup management server to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb2bf-118">-VaultId</span><span class="sxs-lookup"><span data-stu-id="bb2bf-118">-VaultId</span></span>
<span data-ttu-id="bb2bf-119">ID arm do Cofre de Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="bb2bf-119">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="bb2bf-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb2bf-120">CommonParameters</span></span>
<span data-ttu-id="bb2bf-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb2bf-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb2bf-122">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bb2bf-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb2bf-123">Entradas</span><span class="sxs-lookup"><span data-stu-id="bb2bf-123">INPUTS</span></span>

### <span data-ttu-id="bb2bf-124">System.String</span><span class="sxs-lookup"><span data-stu-id="bb2bf-124">System.String</span></span>

## <span data-ttu-id="bb2bf-125">Saídas</span><span class="sxs-lookup"><span data-stu-id="bb2bf-125">OUTPUTS</span></span>

### <span data-ttu-id="bb2bf-126">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupEngineBase</span><span class="sxs-lookup"><span data-stu-id="bb2bf-126">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupEngineBase</span></span>

## <span data-ttu-id="bb2bf-127">Notas</span><span class="sxs-lookup"><span data-stu-id="bb2bf-127">NOTES</span></span>

## <span data-ttu-id="bb2bf-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bb2bf-128">RELATED LINKS</span></span>

[<span data-ttu-id="bb2bf-129">Unregister-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="bb2bf-129">Unregister-AzRecoveryServicesBackupManagementServer</span></span>](./Unregister-AzRecoveryServicesBackupManagementServer.md)


