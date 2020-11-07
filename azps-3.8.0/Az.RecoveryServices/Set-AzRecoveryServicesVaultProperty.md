---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesvaultproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultProperty.md
ms.openlocfilehash: a9bd1eead98a7afb06e1f5b480f8a65fc5079bd4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943521"
---
# <span data-ttu-id="80829-101">Set-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="80829-101">Set-AzRecoveryServicesVaultProperty</span></span>

## <span data-ttu-id="80829-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="80829-102">SYNOPSIS</span></span>
<span data-ttu-id="80829-103">Atualiza as propriedades de um cofre.</span><span class="sxs-lookup"><span data-stu-id="80829-103">Updates properties of a Vault.</span></span>

## <span data-ttu-id="80829-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="80829-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesVaultProperty -SoftDeleteFeatureState <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80829-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="80829-105">DESCRIPTION</span></span>
<span data-ttu-id="80829-106">O cmdlet **set-AzRecoveryServicesVaultProperty** atualiza as propriedades de um cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="80829-106">The **Set-AzRecoveryServicesVaultProperty** cmdlet updates properties of a Recovery services vault.</span></span>
<span data-ttu-id="80829-107">Você pode usar o cmdlet **set-AzRecoveryServicesVaultProperty** para obter as propriedades atuais de um cofre.</span><span class="sxs-lookup"><span data-stu-id="80829-107">You can use **Set-AzRecoveryServicesVaultProperty** cmdlet to get the current properties of a vault.</span></span>
<span data-ttu-id="80829-108">O uso dessa propriedade **SoftDeleteFeatureState** de um cofre pode ser habilitado em qualquer point-in-time.</span><span class="sxs-lookup"><span data-stu-id="80829-108">Using this cmdlet **SoftDeleteFeatureState** property of a vault can be enabled at any point of time.</span></span>
<span data-ttu-id="80829-109">A propriedade **SoftDeleteFeatureState** de um cofre pode ser desabilitada somente se não houver recipientes registrados no cofre.</span><span class="sxs-lookup"><span data-stu-id="80829-109">**SoftDeleteFeatureState** property of a vault can be disabled only if there are no registered containers in the vault.</span></span>
<span data-ttu-id="80829-110">Defina o contexto do cofre usando o cmdlet Set-AzRecoveryServicesVaultContext antes de usar o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="80829-110">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="80829-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="80829-111">EXAMPLES</span></span>

### <span data-ttu-id="80829-112">Exemplo 1: atualizar SoftDeleteFeatureState de um cofre</span><span class="sxs-lookup"><span data-stu-id="80829-112">Example 1: Update SoftDeleteFeatureState of a vault</span></span>
```
PS C:\> $vault = Get-AzRecoveryServicesVault -Name "MyVaultName"
PS C:\> $props = Set-AzRecoveryServicesVaultProperty -VaultId $vault.Id -SoftDeleteFeatureState Enable
```

<span data-ttu-id="80829-113">O primeiro comando obtém um objeto de cofre e, em seguida, armazena-o na variável $vault.</span><span class="sxs-lookup"><span data-stu-id="80829-113">The first command gets a Vault object and then stores it in the $vault variable.</span></span>
<span data-ttu-id="80829-114">O segundo comando atualiza a propriedade SoftDeleteFeatureState do cofre para o estado "habilitado".</span><span class="sxs-lookup"><span data-stu-id="80829-114">The second command Updates the SoftDeleteFeatureState property of the vault to "Enabled" state.</span></span>

## <span data-ttu-id="80829-115">OS</span><span class="sxs-lookup"><span data-stu-id="80829-115">PARAMETERS</span></span>

### <span data-ttu-id="80829-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80829-116">-DefaultProfile</span></span>
<span data-ttu-id="80829-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="80829-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80829-118">-SoftDeleteFeatureState</span><span class="sxs-lookup"><span data-stu-id="80829-118">-SoftDeleteFeatureState</span></span>
<span data-ttu-id="80829-119">SoftDeleteFeatureState do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="80829-119">SoftDeleteFeatureState of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enable, Disable

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80829-120">-Cofreid</span><span class="sxs-lookup"><span data-stu-id="80829-120">-VaultId</span></span>
<span data-ttu-id="80829-121">ID do braço do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="80829-121">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="80829-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="80829-122">-Confirm</span></span>
<span data-ttu-id="80829-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80829-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80829-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80829-124">-WhatIf</span></span>
<span data-ttu-id="80829-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="80829-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="80829-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="80829-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80829-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80829-127">CommonParameters</span></span>
<span data-ttu-id="80829-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80829-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80829-129">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="80829-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80829-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="80829-130">INPUTS</span></span>

### <span data-ttu-id="80829-131">System. String</span><span class="sxs-lookup"><span data-stu-id="80829-131">System.String</span></span>

### <span data-ttu-id="80829-132">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. VaultSoftDeleteFeatureState</span><span class="sxs-lookup"><span data-stu-id="80829-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.VaultSoftDeleteFeatureState</span></span>

## <span data-ttu-id="80829-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="80829-133">OUTPUTS</span></span>

### <span data-ttu-id="80829-134">Microsoft. Azure. Management. Recoveryservices. backup. Models. BackupResourceVaultConfigResource</span><span class="sxs-lookup"><span data-stu-id="80829-134">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span></span>

## <span data-ttu-id="80829-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="80829-135">NOTES</span></span>

## <span data-ttu-id="80829-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="80829-136">RELATED LINKS</span></span>

[<span data-ttu-id="80829-137">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="80829-137">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="80829-138">Get-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="80829-138">Get-AzRecoveryServicesVaultProperty</span></span>](./Get-AzRecoveryServicesVaultProperty.md)


