---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: A10DC2A2-A732-416F-9C68-6533C143AE8F
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/unregister-azrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Unregister-AzRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Unregister-AzRecoveryServicesBackupContainer.md
ms.openlocfilehash: 0da09971892c03c157d9679da8feb88bdd66a73f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941610"
---
# <span data-ttu-id="bdf93-101">Unregister-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="bdf93-101">Unregister-AzRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="bdf93-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bdf93-102">SYNOPSIS</span></span>
<span data-ttu-id="bdf93-103">Cancela o registro de um servidor Windows ou outro contêiner do cofre.</span><span class="sxs-lookup"><span data-stu-id="bdf93-103">Unregisters a Windows Server or other container from the vault.</span></span>

## <span data-ttu-id="bdf93-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bdf93-104">SYNTAX</span></span>

```
Unregister-AzRecoveryServicesBackupContainer [-Container] <ContainerBase> [-PassThru] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bdf93-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bdf93-105">DESCRIPTION</span></span>
<span data-ttu-id="bdf93-106">O cmdlet **Unregister-AzRecoveryServicesBackupContainer** cancela o registro de um servidor Windows ou outro contêiner de backup do cofre.</span><span class="sxs-lookup"><span data-stu-id="bdf93-106">The **Unregister-AzRecoveryServicesBackupContainer** cmdlet unregisters a Windows Server or other Backup container from the vault.</span></span>
<span data-ttu-id="bdf93-107">Esse cmdlet Remove referências a um contêiner do cofre.</span><span class="sxs-lookup"><span data-stu-id="bdf93-107">This cmdlet removes references to a container from the vault.</span></span>
<span data-ttu-id="bdf93-108">Antes de cancelar o registro de um contêiner, você deve excluir todos os dados protegidos associados a esse contêiner.</span><span class="sxs-lookup"><span data-stu-id="bdf93-108">Before you can unregister a container, you must delete any protected data associated with that container.</span></span>
<span data-ttu-id="bdf93-109">Defina o contexto do cofre usando o cmdlet Set-AzRecoveryServicesVaultContext antes de usar o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="bdf93-109">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="bdf93-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bdf93-110">EXAMPLES</span></span>

### <span data-ttu-id="bdf93-111">Exemplo 1: cancelar o registro de um servidor do Windows a partir do cofre</span><span class="sxs-lookup"><span data-stu-id="bdf93-111">Example 1: Unregister a Windows Server from the vault</span></span>
```
PS C:\>$Cont = Get-AzRecoveryServicesBackupContainer -ContainerType "Windows" -BackupManagementType MARS -Name "server01.contoso.com"
PS C:\> Unregister-AzRecoveryServicesBackupContainer -Container $Cont
```

<span data-ttu-id="bdf93-112">O primeiro comando obtém o contêiner do Windows chamado server01.contoso.com que está registrado no cofre e, em seguida, armazena-o na variável $Cont.</span><span class="sxs-lookup"><span data-stu-id="bdf93-112">The first command gets the Windows container named server01.contoso.com that is registered in the vault, and then stores it in the $Cont variable.</span></span>
<span data-ttu-id="bdf93-113">O segundo comando cancela o registro do Windows Server especificado do cofre de backup do Azure.</span><span class="sxs-lookup"><span data-stu-id="bdf93-113">The second command unregisters the specified Windows Server from the Azure Backup vault.</span></span>

## <span data-ttu-id="bdf93-114">OS</span><span class="sxs-lookup"><span data-stu-id="bdf93-114">PARAMETERS</span></span>

### <span data-ttu-id="bdf93-115">-Contêiner</span><span class="sxs-lookup"><span data-stu-id="bdf93-115">-Container</span></span>
<span data-ttu-id="bdf93-116">Especifica um objeto de contêiner de backup para cancelar o registro.</span><span class="sxs-lookup"><span data-stu-id="bdf93-116">Specifies a Backup container object to unregister.</span></span>
<span data-ttu-id="bdf93-117">Para obter um objeto **BackupContainer** , use o cmdlet Get-AzRecoveryServicesBackupContainer.</span><span class="sxs-lookup"><span data-stu-id="bdf93-117">To obtain a **BackupContainer** object, use the Get-AzRecoveryServicesBackupContainer cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bdf93-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdf93-118">-DefaultProfile</span></span>
<span data-ttu-id="bdf93-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bdf93-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bdf93-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bdf93-120">-PassThru</span></span>
<span data-ttu-id="bdf93-121">Retorne o contêiner a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="bdf93-121">Return the container to be deleted.</span></span>

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

### <span data-ttu-id="bdf93-122">-Cofreid</span><span class="sxs-lookup"><span data-stu-id="bdf93-122">-VaultId</span></span>
<span data-ttu-id="bdf93-123">ID do braço do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="bdf93-123">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="bdf93-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="bdf93-124">-Confirm</span></span>
<span data-ttu-id="bdf93-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bdf93-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bdf93-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdf93-126">-WhatIf</span></span>
<span data-ttu-id="bdf93-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bdf93-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bdf93-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bdf93-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bdf93-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdf93-129">CommonParameters</span></span>
<span data-ttu-id="bdf93-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdf93-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdf93-131">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bdf93-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdf93-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bdf93-132">INPUTS</span></span>

### <span data-ttu-id="bdf93-133">System. String</span><span class="sxs-lookup"><span data-stu-id="bdf93-133">System.String</span></span>

## <span data-ttu-id="bdf93-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bdf93-134">OUTPUTS</span></span>

### <span data-ttu-id="bdf93-135">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="bdf93-135">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="bdf93-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bdf93-136">NOTES</span></span>

## <span data-ttu-id="bdf93-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bdf93-137">RELATED LINKS</span></span>

[<span data-ttu-id="bdf93-138">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="bdf93-138">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)


