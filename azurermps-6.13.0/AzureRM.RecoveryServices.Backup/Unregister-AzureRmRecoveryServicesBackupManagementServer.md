---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: BBF12B16-C5FD-4AE2-B5D7-AFDC29CEE4D3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/unregister-azurermrecoveryservicesbackupmanagementserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Unregister-AzureRmRecoveryServicesBackupManagementServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Unregister-AzureRmRecoveryServicesBackupManagementServer.md
ms.openlocfilehash: 4ef306b80aaf5fbb03b5ee4e98104829d8853ba1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602907"
---
# <span data-ttu-id="47faf-101">Unregister-AzureRmRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="47faf-101">Unregister-AzureRmRecoveryServicesBackupManagementServer</span></span>

## <span data-ttu-id="47faf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="47faf-102">SYNOPSIS</span></span>
<span data-ttu-id="47faf-103">Cancela o registro de um servidor SCDPM ou de um servidor de backup do cofre.</span><span class="sxs-lookup"><span data-stu-id="47faf-103">Unregisters a SCDPM server or Backup server from the vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="47faf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="47faf-104">SYNTAX</span></span>

```
Unregister-AzureRmRecoveryServicesBackupManagementServer [-AzureRmBackupManagementServer] <BackupEngineBase>
 [-PassThru] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="47faf-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="47faf-105">DESCRIPTION</span></span>
<span data-ttu-id="47faf-106">O cmdlet **Unregister-AzureRmRecoveryServicesBackupManagementServer** cancela o registro de um servidor de sistema de proteção de dados do System Center (SCDPM) ou um servidor do Azure backup do cofre.</span><span class="sxs-lookup"><span data-stu-id="47faf-106">The **Unregister-AzureRmRecoveryServicesBackupManagementServer** cmdlet unregisters a System Center Data Protection Manager (SCDPM) server or an Azure Backup server from the vault.</span></span>
<span data-ttu-id="47faf-107">Esse cmdlet Remove referências aos servidores que não estão registrados no cofre.</span><span class="sxs-lookup"><span data-stu-id="47faf-107">This cmdlet removes references to the servers that are unregistered from the vault.</span></span>
<span data-ttu-id="47faf-108">Antes de cancelar o registro de um contêiner, você deve excluir todos os dados protegidos associados a esse contêiner.</span><span class="sxs-lookup"><span data-stu-id="47faf-108">Before you can unregister a container, you must delete any protected data associated with that container.</span></span>
<span data-ttu-id="47faf-109">Defina o contexto do cofre usando o cmdlet Set-AzureRmRecoveryServicesVaultContext antes de usar o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="47faf-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="47faf-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="47faf-110">EXAMPLES</span></span>

### <span data-ttu-id="47faf-111">Exemplo 1: cancelar o registro de um servidor SCDPM do cofre</span><span class="sxs-lookup"><span data-stu-id="47faf-111">Example 1: Unregister an SCDPM server from the vault</span></span>
```
PS C:\>$BMS = Get-AzureRmRecoveryServicesBackupManagementServer -Name "dpmserver01.contoso.com"
PS C:\> Unregister-AzureRmRecoveryServicesBackupManagementServer -AzureRmBackupManagementServer $BMS
```

<span data-ttu-id="47faf-112">O primeiro comando obtém o servidor de gerenciamento de backup chamado dpmserver01.contoso.com e, em seguida, armazena-o na variável $BMS.</span><span class="sxs-lookup"><span data-stu-id="47faf-112">The first command gets the Backup management server named dpmserver01.contoso.com, and then stores it in the $BMS variable.</span></span>
<span data-ttu-id="47faf-113">O segundo comando cancela o registro do servidor SCDPM do cofre.</span><span class="sxs-lookup"><span data-stu-id="47faf-113">The second command unregisters the SCDPM server from the vault.</span></span>

## <span data-ttu-id="47faf-114">OS</span><span class="sxs-lookup"><span data-stu-id="47faf-114">PARAMETERS</span></span>

### <span data-ttu-id="47faf-115">-AzureRmBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="47faf-115">-AzureRmBackupManagementServer</span></span>
<span data-ttu-id="47faf-116">Especifica um objeto de servidor SCDPM para cancelar o registro.</span><span class="sxs-lookup"><span data-stu-id="47faf-116">Specifies an SCDPM server object to unregister.</span></span>
<span data-ttu-id="47faf-117">Para obter um objeto **BackupManagementServer** , use o cmdlet Get-AzureRmRecoveryServicesBackupManagementServer.</span><span class="sxs-lookup"><span data-stu-id="47faf-117">To obtain an **BackupManagementServer** object, use the Get-AzureRmRecoveryServicesBackupManagementServer cmdlet.</span></span>

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

### <span data-ttu-id="47faf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47faf-118">-DefaultProfile</span></span>
<span data-ttu-id="47faf-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="47faf-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47faf-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="47faf-120">-PassThru</span></span>
<span data-ttu-id="47faf-121">Retorne o servidor de gerenciamento de backup a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="47faf-121">Return the Backup Management Server to be deleted.</span></span>

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

### <span data-ttu-id="47faf-122">-Cofreid</span><span class="sxs-lookup"><span data-stu-id="47faf-122">-VaultId</span></span>
<span data-ttu-id="47faf-123">ID do braço do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="47faf-123">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="47faf-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="47faf-124">-Confirm</span></span>
<span data-ttu-id="47faf-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47faf-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47faf-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47faf-126">-WhatIf</span></span>
<span data-ttu-id="47faf-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="47faf-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="47faf-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="47faf-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47faf-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47faf-129">CommonParameters</span></span>
<span data-ttu-id="47faf-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47faf-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47faf-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47faf-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47faf-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="47faf-132">INPUTS</span></span>

### <span data-ttu-id="47faf-133">System. String</span><span class="sxs-lookup"><span data-stu-id="47faf-133">System.String</span></span>
<span data-ttu-id="47faf-134">Parâmetros: Vaultid (ByValue)</span><span class="sxs-lookup"><span data-stu-id="47faf-134">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="47faf-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="47faf-135">OUTPUTS</span></span>

### <span data-ttu-id="47faf-136">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. BackupEngineBase</span><span class="sxs-lookup"><span data-stu-id="47faf-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupEngineBase</span></span>

## <span data-ttu-id="47faf-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="47faf-137">NOTES</span></span>

## <span data-ttu-id="47faf-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="47faf-138">RELATED LINKS</span></span>

[<span data-ttu-id="47faf-139">Get-AzureRmRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="47faf-139">Get-AzureRmRecoveryServicesBackupManagementServer</span></span>](./Get-AzureRmRecoveryServicesBackupManagementServer.md)


