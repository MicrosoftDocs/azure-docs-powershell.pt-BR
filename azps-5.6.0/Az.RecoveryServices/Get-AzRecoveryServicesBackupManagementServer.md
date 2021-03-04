---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 4B7ACEC8-29BB-4791-8087-801300F246B4
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupmanagementserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupManagementServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupManagementServer.md
ms.openlocfilehash: 50fb3af805adf4e42ab0b6bf1824b09473d98239
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890362"
---
# <span data-ttu-id="409c2-101">Get-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="409c2-101">Get-AzRecoveryServicesBackupManagementServer</span></span>

## <span data-ttu-id="409c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="409c2-102">SYNOPSIS</span></span>
<span data-ttu-id="409c2-103">Obtém servidores de gerenciamento do SCDPM e do Azure Backup.</span><span class="sxs-lookup"><span data-stu-id="409c2-103">Gets SCDPM and Azure Backup management servers.</span></span>

## <span data-ttu-id="409c2-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="409c2-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupManagementServer [[-Name] <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="409c2-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="409c2-105">DESCRIPTION</span></span>
<span data-ttu-id="409c2-106">O cmdlet **Get-AzRecoveryServicesBackupManagementServer** obtém uma lista de servidores de gerenciamento de backup registrados em um cofre.</span><span class="sxs-lookup"><span data-stu-id="409c2-106">The **Get-AzRecoveryServicesBackupManagementServer** cmdlet gets a list of Backup management servers that are registered in a vault.</span></span>
<span data-ttu-id="409c2-107">Há dois tipos de servidores de gerenciamento de backup: o System Center Data Protection Manager (SCDPM) e os servidores de gerenciamento de Backup do Azure.</span><span class="sxs-lookup"><span data-stu-id="409c2-107">There are two types of Backup management servers: System Center Data Protection Manager (SCDPM) and Azure Backup management servers.</span></span>
<span data-ttu-id="409c2-108">Os servidores de gerenciamento de backup são instalados separadamente para gerenciar a orquestração de backup.</span><span class="sxs-lookup"><span data-stu-id="409c2-108">Backup management servers are installed separately to manage Backup orchestration.</span></span>
<span data-ttu-id="409c2-109">De definir o contexto do cofre usando o cmdlet Set-AzRecoveryServicesVaultContext antes de usar o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="409c2-109">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="409c2-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="409c2-110">EXAMPLES</span></span>

### <span data-ttu-id="409c2-111">Exemplo 1: Obter todos os servidores de gerenciamento de backup</span><span class="sxs-lookup"><span data-stu-id="409c2-111">Example 1: Get all Backup management servers</span></span>
```
PS C:\>Get-AzRecoveryServicesBackupManagementServer
```

<span data-ttu-id="409c2-112">Esse comando obtém todos os servidores de gerenciamento de backup registrados no cofre.</span><span class="sxs-lookup"><span data-stu-id="409c2-112">This command gets all Backup management servers registered with the vault.</span></span>

## <span data-ttu-id="409c2-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="409c2-113">PARAMETERS</span></span>

### <span data-ttu-id="409c2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="409c2-114">-DefaultProfile</span></span>
<span data-ttu-id="409c2-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="409c2-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="409c2-116">-Name</span><span class="sxs-lookup"><span data-stu-id="409c2-116">-Name</span></span>
<span data-ttu-id="409c2-117">Especifica o nome do servidor de gerenciamento de backup a ser obter.</span><span class="sxs-lookup"><span data-stu-id="409c2-117">Specifies the name of the Backup management server to get.</span></span>

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

### <span data-ttu-id="409c2-118">-VaultId</span><span class="sxs-lookup"><span data-stu-id="409c2-118">-VaultId</span></span>
<span data-ttu-id="409c2-119">ARM ID do Cofre de Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="409c2-119">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="409c2-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="409c2-120">CommonParameters</span></span>
<span data-ttu-id="409c2-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="409c2-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="409c2-122">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="409c2-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="409c2-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="409c2-123">INPUTS</span></span>

### <span data-ttu-id="409c2-124">System.String</span><span class="sxs-lookup"><span data-stu-id="409c2-124">System.String</span></span>

## <span data-ttu-id="409c2-125">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="409c2-125">OUTPUTS</span></span>

### <span data-ttu-id="409c2-126">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupEngineBase</span><span class="sxs-lookup"><span data-stu-id="409c2-126">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupEngineBase</span></span>

## <span data-ttu-id="409c2-127">NOTES</span><span class="sxs-lookup"><span data-stu-id="409c2-127">NOTES</span></span>

## <span data-ttu-id="409c2-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="409c2-128">RELATED LINKS</span></span>

[<span data-ttu-id="409c2-129">Unregister-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="409c2-129">Unregister-AzRecoveryServicesBackupManagementServer</span></span>](./Unregister-AzRecoveryServicesBackupManagementServer.md)


