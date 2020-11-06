---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: BBF12B16-C5FD-4AE2-B5D7-AFDC29CEE4D3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Unregister-AzureRmRecoveryServicesBackupManagementServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Unregister-AzureRmRecoveryServicesBackupManagementServer.md
ms.openlocfilehash: 1b025825878e2bc97837237e194b0ec37eb298d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433045"
---
# <span data-ttu-id="25246-101">Unregister-AzureRmRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="25246-101">Unregister-AzureRmRecoveryServicesBackupManagementServer</span></span>

## <span data-ttu-id="25246-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="25246-102">SYNOPSIS</span></span>
<span data-ttu-id="25246-103">Cancela o registro de um servidor SCDPM ou de um servidor de backup do cofre.</span><span class="sxs-lookup"><span data-stu-id="25246-103">Unregisters a SCDPM server or Backup server from the vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25246-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="25246-104">SYNTAX</span></span>

```
Unregister-AzureRmRecoveryServicesBackupManagementServer [-AzureRmBackupManagementServer] <BackupEngineBase>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25246-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="25246-105">DESCRIPTION</span></span>
<span data-ttu-id="25246-106">O cmdlet **Unregister-AzureRmRecoveryServicesBackupManagementServer** cancela o registro de um servidor de sistema de proteção de dados do System Center (SCDPM) ou um servidor do Azure backup do cofre.</span><span class="sxs-lookup"><span data-stu-id="25246-106">The **Unregister-AzureRmRecoveryServicesBackupManagementServer** cmdlet unregisters a System Center Data Protection Manager (SCDPM) server or an Azure Backup server from the vault.</span></span>
<span data-ttu-id="25246-107">Esse cmdlet Remove referências aos servidores que não estão registrados no cofre.</span><span class="sxs-lookup"><span data-stu-id="25246-107">This cmdlet removes references to the servers that are unregistered from the vault.</span></span>

<span data-ttu-id="25246-108">Antes de cancelar o registro de um contêiner, você deve excluir todos os dados protegidos associados a esse contêiner.</span><span class="sxs-lookup"><span data-stu-id="25246-108">Before you can unregister a container, you must delete any protected data associated with that container.</span></span>

<span data-ttu-id="25246-109">Defina o contexto do cofre usando o cmdlet Set-AzureRmRecoveryServicesVaultContext antes de usar o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="25246-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="25246-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="25246-110">EXAMPLES</span></span>

### <span data-ttu-id="25246-111">Exemplo 1: cancelar o registro de um servidor SCDPM do cofre</span><span class="sxs-lookup"><span data-stu-id="25246-111">Example 1: Unregister an SCDPM server from the vault</span></span>
```
PS C:\>$BMS = Get-AzureRmRecoveryServicesBackupManagementServer -Name "dpmserver01.contoso.com"
PS C:\> Unregister-AzureRmRecoveryServicesBackupManagementServer -AzureRmBackupManagementServer $BMS
```

<span data-ttu-id="25246-112">O primeiro comando obtém o servidor de gerenciamento de backup chamado dpmserver01.contoso.com e, em seguida, armazena-o na variável $BMS.</span><span class="sxs-lookup"><span data-stu-id="25246-112">The first command gets the Backup management server named dpmserver01.contoso.com, and then stores it in the $BMS variable.</span></span>

<span data-ttu-id="25246-113">O segundo comando cancela o registro do servidor SCDPM do cofre.</span><span class="sxs-lookup"><span data-stu-id="25246-113">The second command unregisters the SCDPM server from the vault.</span></span>

## <span data-ttu-id="25246-114">OS</span><span class="sxs-lookup"><span data-stu-id="25246-114">PARAMETERS</span></span>

### <span data-ttu-id="25246-115">-AzureRmBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="25246-115">-AzureRmBackupManagementServer</span></span>
<span data-ttu-id="25246-116">Especifica um objeto de servidor SCDPM para cancelar o registro.</span><span class="sxs-lookup"><span data-stu-id="25246-116">Specifies an SCDPM server object to unregister.</span></span>
<span data-ttu-id="25246-117">Para obter um objeto **BackupManagementServer** , use o cmdlet Get-AzureRmRecoveryServicesBackupManagementServer.</span><span class="sxs-lookup"><span data-stu-id="25246-117">To obtain an **BackupManagementServer** object, use the Get-AzureRmRecoveryServicesBackupManagementServer cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupEngineBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25246-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25246-118">-DefaultProfile</span></span>
<span data-ttu-id="25246-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="25246-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25246-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25246-120">CommonParameters</span></span>
<span data-ttu-id="25246-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25246-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25246-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25246-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25246-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="25246-123">INPUTS</span></span>

## <span data-ttu-id="25246-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="25246-124">OUTPUTS</span></span>

## <span data-ttu-id="25246-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="25246-125">NOTES</span></span>

## <span data-ttu-id="25246-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="25246-126">RELATED LINKS</span></span>

[<span data-ttu-id="25246-127">Get-AzureRmRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="25246-127">Get-AzureRmRecoveryServicesBackupManagementServer</span></span>](./Get-AzureRmRecoveryServicesBackupManagementServer.md)


