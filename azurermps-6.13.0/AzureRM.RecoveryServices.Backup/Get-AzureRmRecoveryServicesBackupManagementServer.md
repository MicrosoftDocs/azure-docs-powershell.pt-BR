---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 4B7ACEC8-29BB-4791-8087-801300F246B4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupmanagementserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupManagementServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupManagementServer.md
ms.openlocfilehash: c3419f020aca0853d94d8848e944e39fc8ed05a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430086"
---
# <span data-ttu-id="0d6d6-101">Get-AzureRmRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="0d6d6-101">Get-AzureRmRecoveryServicesBackupManagementServer</span></span>

## <span data-ttu-id="0d6d6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0d6d6-102">SYNOPSIS</span></span>
<span data-ttu-id="0d6d6-103">Obtém servidores de gerenciamento de backup do SCDPM e do Azure.</span><span class="sxs-lookup"><span data-stu-id="0d6d6-103">Gets SCDPM and Azure Backup management servers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d6d6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0d6d6-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupManagementServer [[-Name] <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d6d6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0d6d6-105">DESCRIPTION</span></span>
<span data-ttu-id="0d6d6-106">O cmdlet **Get-AzureRmRecoveryServicesBackupManagementServer** Obtém uma lista de servidores de gerenciamento de backup que são registrados em um cofre.</span><span class="sxs-lookup"><span data-stu-id="0d6d6-106">The **Get-AzureRmRecoveryServicesBackupManagementServer** cmdlet gets a list of Backup management servers that are registered in a vault.</span></span>
<span data-ttu-id="0d6d6-107">Há dois tipos de servidores de gerenciamento de backup: o System Center Data Protection Manager (SCDPM) e os servidores de gerenciamento de backup do Azure.</span><span class="sxs-lookup"><span data-stu-id="0d6d6-107">There are two types of Backup management servers: System Center Data Protection Manager (SCDPM) and Azure Backup management servers.</span></span>
<span data-ttu-id="0d6d6-108">Os servidores de gerenciamento de backup são instalados separadamente para gerenciar a orquestração de backup.</span><span class="sxs-lookup"><span data-stu-id="0d6d6-108">Backup management servers are installed separately to manage Backup orchestration.</span></span>
<span data-ttu-id="0d6d6-109">Defina o contexto do cofre usando o cmdlet Set-AzureRmRecoveryServicesVaultContext antes de usar o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="0d6d6-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="0d6d6-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0d6d6-110">EXAMPLES</span></span>

### <span data-ttu-id="0d6d6-111">Exemplo 1: obter todos os servidores de gerenciamento de backup</span><span class="sxs-lookup"><span data-stu-id="0d6d6-111">Example 1: Get all Backup management servers</span></span>
```
PS C:\>Get-AzureRmRecoveryServicesBackupManagementServer
```

<span data-ttu-id="0d6d6-112">Esse comando obtém todos os servidores de gerenciamento de backup registrados no cofre.</span><span class="sxs-lookup"><span data-stu-id="0d6d6-112">This command gets all Backup management servers registered with the vault.</span></span>

## <span data-ttu-id="0d6d6-113">OS</span><span class="sxs-lookup"><span data-stu-id="0d6d6-113">PARAMETERS</span></span>

### <span data-ttu-id="0d6d6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d6d6-114">-DefaultProfile</span></span>
<span data-ttu-id="0d6d6-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0d6d6-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d6d6-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="0d6d6-116">-Name</span></span>
<span data-ttu-id="0d6d6-117">Especifica o nome do servidor de gerenciamento de backup a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="0d6d6-117">Specifies the name of the Backup management server to get.</span></span>

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

### <span data-ttu-id="0d6d6-118">-Cofreid</span><span class="sxs-lookup"><span data-stu-id="0d6d6-118">-VaultId</span></span>
<span data-ttu-id="0d6d6-119">ID do braço do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="0d6d6-119">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="0d6d6-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d6d6-120">CommonParameters</span></span>
<span data-ttu-id="0d6d6-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d6d6-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d6d6-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d6d6-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d6d6-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0d6d6-123">INPUTS</span></span>

### <span data-ttu-id="0d6d6-124">System. String</span><span class="sxs-lookup"><span data-stu-id="0d6d6-124">System.String</span></span>
<span data-ttu-id="0d6d6-125">Parâmetros: Vaultid (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0d6d6-125">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="0d6d6-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0d6d6-126">OUTPUTS</span></span>

### <span data-ttu-id="0d6d6-127">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. BackupEngineBase</span><span class="sxs-lookup"><span data-stu-id="0d6d6-127">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupEngineBase</span></span>

## <span data-ttu-id="0d6d6-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0d6d6-128">NOTES</span></span>

## <span data-ttu-id="0d6d6-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0d6d6-129">RELATED LINKS</span></span>

[<span data-ttu-id="0d6d6-130">Cancelar registro-AzureRmRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="0d6d6-130">Unregister-AzureRmRecoveryServicesBackupManagementServer</span></span>](./Unregister-AzureRmRecoveryServicesBackupManagementServer.md)

