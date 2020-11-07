---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 4B7ACEC8-29BB-4791-8087-801300F246B4
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupmanagementserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupManagementServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupManagementServer.md
ms.openlocfilehash: 341b222c8b5e85a4b5f5221c34d6f45cd2993c71
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773009"
---
# <span data-ttu-id="764a4-101">Get-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="764a4-101">Get-AzRecoveryServicesBackupManagementServer</span></span>

## <span data-ttu-id="764a4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="764a4-102">SYNOPSIS</span></span>
<span data-ttu-id="764a4-103">Obtém servidores de gerenciamento de backup do SCDPM e do Azure.</span><span class="sxs-lookup"><span data-stu-id="764a4-103">Gets SCDPM and Azure Backup management servers.</span></span>

## <span data-ttu-id="764a4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="764a4-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupManagementServer [[-Name] <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="764a4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="764a4-105">DESCRIPTION</span></span>
<span data-ttu-id="764a4-106">O cmdlet **Get-AzRecoveryServicesBackupManagementServer** Obtém uma lista de servidores de gerenciamento de backup que são registrados em um cofre.</span><span class="sxs-lookup"><span data-stu-id="764a4-106">The **Get-AzRecoveryServicesBackupManagementServer** cmdlet gets a list of Backup management servers that are registered in a vault.</span></span>
<span data-ttu-id="764a4-107">Há dois tipos de servidores de gerenciamento de backup: o System Center Data Protection Manager (SCDPM) e os servidores de gerenciamento de backup do Azure.</span><span class="sxs-lookup"><span data-stu-id="764a4-107">There are two types of Backup management servers: System Center Data Protection Manager (SCDPM) and Azure Backup management servers.</span></span>
<span data-ttu-id="764a4-108">Os servidores de gerenciamento de backup são instalados separadamente para gerenciar a orquestração de backup.</span><span class="sxs-lookup"><span data-stu-id="764a4-108">Backup management servers are installed separately to manage Backup orchestration.</span></span>
<span data-ttu-id="764a4-109">Defina o contexto do cofre usando o cmdlet Set-AzRecoveryServicesVaultContext antes de usar o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="764a4-109">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="764a4-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="764a4-110">EXAMPLES</span></span>

### <span data-ttu-id="764a4-111">Exemplo 1: obter todos os servidores de gerenciamento de backup</span><span class="sxs-lookup"><span data-stu-id="764a4-111">Example 1: Get all Backup management servers</span></span>
```
PS C:\>Get-AzRecoveryServicesBackupManagementServer
```

<span data-ttu-id="764a4-112">Esse comando obtém todos os servidores de gerenciamento de backup registrados no cofre.</span><span class="sxs-lookup"><span data-stu-id="764a4-112">This command gets all Backup management servers registered with the vault.</span></span>

## <span data-ttu-id="764a4-113">OS</span><span class="sxs-lookup"><span data-stu-id="764a4-113">PARAMETERS</span></span>

### <span data-ttu-id="764a4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="764a4-114">-DefaultProfile</span></span>
<span data-ttu-id="764a4-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="764a4-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="764a4-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="764a4-116">-Name</span></span>
<span data-ttu-id="764a4-117">Especifica o nome do servidor de gerenciamento de backup a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="764a4-117">Specifies the name of the Backup management server to get.</span></span>

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

### <span data-ttu-id="764a4-118">-Cofreid</span><span class="sxs-lookup"><span data-stu-id="764a4-118">-VaultId</span></span>
<span data-ttu-id="764a4-119">ID do braço do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="764a4-119">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="764a4-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="764a4-120">CommonParameters</span></span>
<span data-ttu-id="764a4-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="764a4-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="764a4-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="764a4-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="764a4-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="764a4-123">INPUTS</span></span>

### <span data-ttu-id="764a4-124">System. String</span><span class="sxs-lookup"><span data-stu-id="764a4-124">System.String</span></span>

## <span data-ttu-id="764a4-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="764a4-125">OUTPUTS</span></span>

### <span data-ttu-id="764a4-126">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. BackupEngineBase</span><span class="sxs-lookup"><span data-stu-id="764a4-126">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupEngineBase</span></span>

## <span data-ttu-id="764a4-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="764a4-127">NOTES</span></span>

## <span data-ttu-id="764a4-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="764a4-128">RELATED LINKS</span></span>

[<span data-ttu-id="764a4-129">Cancelar registro-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="764a4-129">Unregister-AzRecoveryServicesBackupManagementServer</span></span>](./Unregister-AzRecoveryServicesBackupManagementServer.md)


