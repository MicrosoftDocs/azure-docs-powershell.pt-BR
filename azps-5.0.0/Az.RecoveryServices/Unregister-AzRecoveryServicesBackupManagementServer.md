---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: BBF12B16-C5FD-4AE2-B5D7-AFDC29CEE4D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/unregister-azrecoveryservicesbackupmanagementserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Unregister-AzRecoveryServicesBackupManagementServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Unregister-AzRecoveryServicesBackupManagementServer.md
ms.openlocfilehash: cc52435ff0b288656e4a917620659737f33916ca
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94116843"
---
# <span data-ttu-id="fa05d-101">Unregister-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="fa05d-101">Unregister-AzRecoveryServicesBackupManagementServer</span></span>

## <span data-ttu-id="fa05d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fa05d-102">SYNOPSIS</span></span>
<span data-ttu-id="fa05d-103">Cancela o registro de um servidor SCDPM ou de um servidor de backup do cofre.</span><span class="sxs-lookup"><span data-stu-id="fa05d-103">Unregisters a SCDPM server or Backup server from the vault.</span></span>

## <span data-ttu-id="fa05d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fa05d-104">SYNTAX</span></span>

```
Unregister-AzRecoveryServicesBackupManagementServer [-AzureRmBackupManagementServer] <BackupEngineBase>
 [-PassThru] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fa05d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fa05d-105">DESCRIPTION</span></span>
<span data-ttu-id="fa05d-106">O cmdlet **Unregister-AzRecoveryServicesBackupManagementServer** cancela o registro de um servidor de sistema de proteção de dados do System Center (SCDPM) ou um servidor do Azure backup do cofre.</span><span class="sxs-lookup"><span data-stu-id="fa05d-106">The **Unregister-AzRecoveryServicesBackupManagementServer** cmdlet unregisters a System Center Data Protection Manager (SCDPM) server or an Azure Backup server from the vault.</span></span>
<span data-ttu-id="fa05d-107">Esse cmdlet Remove referências aos servidores que não estão registrados no cofre.</span><span class="sxs-lookup"><span data-stu-id="fa05d-107">This cmdlet removes references to the servers that are unregistered from the vault.</span></span>
<span data-ttu-id="fa05d-108">Antes de cancelar o registro de um contêiner, você deve excluir todos os dados protegidos associados a esse contêiner.</span><span class="sxs-lookup"><span data-stu-id="fa05d-108">Before you can unregister a container, you must delete any protected data associated with that container.</span></span>
<span data-ttu-id="fa05d-109">Defina o contexto do cofre usando o cmdlet Set-AzRecoveryServicesVaultContext antes de usar o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="fa05d-109">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="fa05d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fa05d-110">EXAMPLES</span></span>

### <span data-ttu-id="fa05d-111">Exemplo 1: cancelar o registro de um servidor SCDPM do cofre</span><span class="sxs-lookup"><span data-stu-id="fa05d-111">Example 1: Unregister an SCDPM server from the vault</span></span>
```powershell
PS C:\>$BMS = Get-AzRecoveryServicesBackupManagementServer -Name "dpmserver01.contoso.com"
PS C:\> Unregister-AzRecoveryServicesBackupManagementServer -AzBackupManagementServer $BMS
```

<span data-ttu-id="fa05d-112">O primeiro comando obtém o servidor de gerenciamento de backup chamado dpmserver01.contoso.com e, em seguida, armazena-o na variável $BMS.</span><span class="sxs-lookup"><span data-stu-id="fa05d-112">The first command gets the Backup management server named dpmserver01.contoso.com, and then stores it in the $BMS variable.</span></span>
<span data-ttu-id="fa05d-113">O segundo comando cancela o registro do servidor SCDPM do cofre.</span><span class="sxs-lookup"><span data-stu-id="fa05d-113">The second command unregisters the SCDPM server from the vault.</span></span>

### <span data-ttu-id="fa05d-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="fa05d-114">Example 2</span></span>

<span data-ttu-id="fa05d-115">Cancela o registro de um servidor SCDPM ou de um servidor de backup do cofre.</span><span class="sxs-lookup"><span data-stu-id="fa05d-115">Unregisters a SCDPM server or Backup server from the vault.</span></span> <span data-ttu-id="fa05d-116">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="fa05d-116">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Unregister-AzRecoveryServicesBackupManagementServer -AzureRmBackupManagementServer <BackupEngineBase> -VaultId $vault.ID
```

## <span data-ttu-id="fa05d-117">OS</span><span class="sxs-lookup"><span data-stu-id="fa05d-117">PARAMETERS</span></span>

### <span data-ttu-id="fa05d-118">-AzureRmBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="fa05d-118">-AzureRmBackupManagementServer</span></span>
<span data-ttu-id="fa05d-119">O contêiner de backup dos serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="fa05d-119">The recovery services backup container.</span></span>

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

### <span data-ttu-id="fa05d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa05d-120">-DefaultProfile</span></span>
<span data-ttu-id="fa05d-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fa05d-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fa05d-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fa05d-122">-PassThru</span></span>
<span data-ttu-id="fa05d-123">Retorne o servidor de gerenciamento de backup a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="fa05d-123">Return the Backup Management Server to be deleted.</span></span>

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

### <span data-ttu-id="fa05d-124">-Cofreid</span><span class="sxs-lookup"><span data-stu-id="fa05d-124">-VaultId</span></span>
<span data-ttu-id="fa05d-125">ID do braço do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="fa05d-125">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="fa05d-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fa05d-126">-Confirm</span></span>
<span data-ttu-id="fa05d-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa05d-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa05d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa05d-128">-WhatIf</span></span>
<span data-ttu-id="fa05d-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fa05d-129">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="fa05d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa05d-130">CommonParameters</span></span>
<span data-ttu-id="fa05d-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa05d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa05d-132">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fa05d-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa05d-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fa05d-133">INPUTS</span></span>

### <span data-ttu-id="fa05d-134">System. String</span><span class="sxs-lookup"><span data-stu-id="fa05d-134">System.String</span></span>

## <span data-ttu-id="fa05d-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fa05d-135">OUTPUTS</span></span>

### <span data-ttu-id="fa05d-136">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. BackupEngineBase</span><span class="sxs-lookup"><span data-stu-id="fa05d-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupEngineBase</span></span>

## <span data-ttu-id="fa05d-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fa05d-137">NOTES</span></span>

## <span data-ttu-id="fa05d-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fa05d-138">RELATED LINKS</span></span>

[<span data-ttu-id="fa05d-139">Get-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="fa05d-139">Get-AzRecoveryServicesBackupManagementServer</span></span>](./Get-AzRecoveryServicesBackupManagementServer.md)


