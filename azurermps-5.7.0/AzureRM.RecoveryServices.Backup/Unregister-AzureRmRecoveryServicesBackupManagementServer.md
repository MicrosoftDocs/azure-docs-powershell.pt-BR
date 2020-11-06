---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: BBF12B16-C5FD-4AE2-B5D7-AFDC29CEE4D3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/unregister-azurermrecoveryservicesbackupmanagementserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Unregister-AzureRmRecoveryServicesBackupManagementServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Unregister-AzureRmRecoveryServicesBackupManagementServer.md
ms.openlocfilehash: 7612a816db41e3befb58cc739bcc78e2d27ec8d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427473"
---
# <span data-ttu-id="1e288-101">Unregister-AzureRmRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="1e288-101">Unregister-AzureRmRecoveryServicesBackupManagementServer</span></span>

## <span data-ttu-id="1e288-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1e288-102">SYNOPSIS</span></span>
<span data-ttu-id="1e288-103">Cancela o registro de um servidor SCDPM ou de um servidor de backup do cofre.</span><span class="sxs-lookup"><span data-stu-id="1e288-103">Unregisters a SCDPM server or Backup server from the vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1e288-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1e288-104">SYNTAX</span></span>

```
Unregister-AzureRmRecoveryServicesBackupManagementServer [-AzureRmBackupManagementServer] <BackupEngineBase>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e288-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1e288-105">DESCRIPTION</span></span>
<span data-ttu-id="1e288-106">O cmdlet **Unregister-AzureRmRecoveryServicesBackupManagementServer** cancela o registro de um servidor de sistema de proteção de dados do System Center (SCDPM) ou um servidor do Azure backup do cofre.</span><span class="sxs-lookup"><span data-stu-id="1e288-106">The **Unregister-AzureRmRecoveryServicesBackupManagementServer** cmdlet unregisters a System Center Data Protection Manager (SCDPM) server or an Azure Backup server from the vault.</span></span>
<span data-ttu-id="1e288-107">Esse cmdlet Remove referências aos servidores que não estão registrados no cofre.</span><span class="sxs-lookup"><span data-stu-id="1e288-107">This cmdlet removes references to the servers that are unregistered from the vault.</span></span>

<span data-ttu-id="1e288-108">Antes de cancelar o registro de um contêiner, você deve excluir todos os dados protegidos associados a esse contêiner.</span><span class="sxs-lookup"><span data-stu-id="1e288-108">Before you can unregister a container, you must delete any protected data associated with that container.</span></span>

<span data-ttu-id="1e288-109">Defina o contexto do cofre usando o cmdlet Set-AzureRmRecoveryServicesVaultContext antes de usar o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="1e288-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="1e288-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1e288-110">EXAMPLES</span></span>

### <span data-ttu-id="1e288-111">Exemplo 1: cancelar o registro de um servidor SCDPM do cofre</span><span class="sxs-lookup"><span data-stu-id="1e288-111">Example 1: Unregister an SCDPM server from the vault</span></span>
```
PS C:\>$BMS = Get-AzureRmRecoveryServicesBackupManagementServer -Name "dpmserver01.contoso.com"
PS C:\> Unregister-AzureRmRecoveryServicesBackupManagementServer -AzureRmBackupManagementServer $BMS
```

<span data-ttu-id="1e288-112">O primeiro comando obtém o servidor de gerenciamento de backup chamado dpmserver01.contoso.com e, em seguida, armazena-o na variável $BMS.</span><span class="sxs-lookup"><span data-stu-id="1e288-112">The first command gets the Backup management server named dpmserver01.contoso.com, and then stores it in the $BMS variable.</span></span>

<span data-ttu-id="1e288-113">O segundo comando cancela o registro do servidor SCDPM do cofre.</span><span class="sxs-lookup"><span data-stu-id="1e288-113">The second command unregisters the SCDPM server from the vault.</span></span>

## <span data-ttu-id="1e288-114">OS</span><span class="sxs-lookup"><span data-stu-id="1e288-114">PARAMETERS</span></span>

### <span data-ttu-id="1e288-115">-AzureRmBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="1e288-115">-AzureRmBackupManagementServer</span></span>
<span data-ttu-id="1e288-116">Especifica um objeto de servidor SCDPM para cancelar o registro.</span><span class="sxs-lookup"><span data-stu-id="1e288-116">Specifies an SCDPM server object to unregister.</span></span>
<span data-ttu-id="1e288-117">Para obter um objeto **BackupManagementServer** , use o cmdlet Get-AzureRmRecoveryServicesBackupManagementServer.</span><span class="sxs-lookup"><span data-stu-id="1e288-117">To obtain an **BackupManagementServer** object, use the Get-AzureRmRecoveryServicesBackupManagementServer cmdlet.</span></span>

```yaml
Type: BackupEngineBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e288-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e288-118">-DefaultProfile</span></span>
<span data-ttu-id="1e288-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1e288-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e288-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1e288-120">-PassThru</span></span>
<span data-ttu-id="1e288-121">Retorne o servidor de gerenciamento de backup a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="1e288-121">Return the Backup Management Server to be deleted.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e288-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1e288-122">-Confirm</span></span>
<span data-ttu-id="1e288-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e288-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e288-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e288-124">-WhatIf</span></span>
<span data-ttu-id="1e288-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1e288-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1e288-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1e288-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e288-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e288-127">CommonParameters</span></span>
<span data-ttu-id="1e288-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e288-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e288-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e288-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e288-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1e288-130">INPUTS</span></span>

### <span data-ttu-id="1e288-131">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="1e288-131">None</span></span>
<span data-ttu-id="1e288-132">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="1e288-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1e288-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1e288-133">OUTPUTS</span></span>

## <span data-ttu-id="1e288-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1e288-134">NOTES</span></span>

## <span data-ttu-id="1e288-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1e288-135">RELATED LINKS</span></span>

[<span data-ttu-id="1e288-136">Get-AzureRmRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="1e288-136">Get-AzureRmRecoveryServicesBackupManagementServer</span></span>](./Get-AzureRmRecoveryServicesBackupManagementServer.md)


