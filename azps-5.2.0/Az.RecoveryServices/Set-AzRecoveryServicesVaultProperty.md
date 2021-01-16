---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesvaultproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultProperty.md
ms.openlocfilehash: 4b34bdf2357b389081297df8f49745127953985b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98264236"
---
# <span data-ttu-id="8232a-101">Set-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="8232a-101">Set-AzRecoveryServicesVaultProperty</span></span>

## <span data-ttu-id="8232a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8232a-102">SYNOPSIS</span></span>
<span data-ttu-id="8232a-103">Atualiza as propriedades de um cofre.</span><span class="sxs-lookup"><span data-stu-id="8232a-103">Updates properties of a Vault.</span></span>

## <span data-ttu-id="8232a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8232a-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesVaultProperty -SoftDeleteFeatureState <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8232a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8232a-105">DESCRIPTION</span></span>
<span data-ttu-id="8232a-106">O cmdlet **set-AzRecoveryServicesVaultProperty** atualiza as propriedades de um cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="8232a-106">The **Set-AzRecoveryServicesVaultProperty** cmdlet updates properties of a Recovery services vault.</span></span>
<span data-ttu-id="8232a-107">Esse cmdlet retorna as propriedades do cofre atualizadas após a operação de conjunto atual.</span><span class="sxs-lookup"><span data-stu-id="8232a-107">This cmdlet returns the updated vault properties after the current set operation.</span></span>
<span data-ttu-id="8232a-108">O uso dessas propriedades de cofre, como exclusão suave, pode ser habilitado em qualquer point-in-time.</span><span class="sxs-lookup"><span data-stu-id="8232a-108">Using this cmdlet properties of vault such as soft-delete can be enabled at any point of time.</span></span>
<span data-ttu-id="8232a-109">A propriedade **SoftDeleteFeatureState** de um cofre pode ser desabilitada somente se não houver recipientes registrados no cofre.</span><span class="sxs-lookup"><span data-stu-id="8232a-109">**SoftDeleteFeatureState** property of a vault can be disabled only if there are no registered containers in the vault.</span></span>

## <span data-ttu-id="8232a-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8232a-110">EXAMPLES</span></span>

### <span data-ttu-id="8232a-111">Exemplo 1: atualizar SoftDeleteFeatureState de um cofre</span><span class="sxs-lookup"><span data-stu-id="8232a-111">Example 1: Update SoftDeleteFeatureState of a vault</span></span>
```
PS C:\> $vault = Get-AzRecoveryServicesVault -Name "MyVaultName"
PS C:\> $props = Set-AzRecoveryServicesVaultProperty -VaultId $vault.Id -SoftDeleteFeatureState Enable
```

<span data-ttu-id="8232a-112">O primeiro comando obtém um objeto de cofre e, em seguida, armazena-o na variável $vault.</span><span class="sxs-lookup"><span data-stu-id="8232a-112">The first command gets a Vault object and then stores it in the $vault variable.</span></span>
<span data-ttu-id="8232a-113">O segundo comando atualiza a propriedade SoftDeleteFeatureState do cofre para o estado "habilitado".</span><span class="sxs-lookup"><span data-stu-id="8232a-113">The second command Updates the SoftDeleteFeatureState property of the vault to "Enabled" state.</span></span>

## <span data-ttu-id="8232a-114">OS</span><span class="sxs-lookup"><span data-stu-id="8232a-114">PARAMETERS</span></span>

### <span data-ttu-id="8232a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8232a-115">-DefaultProfile</span></span>
<span data-ttu-id="8232a-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8232a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8232a-117">-SoftDeleteFeatureState</span><span class="sxs-lookup"><span data-stu-id="8232a-117">-SoftDeleteFeatureState</span></span>
<span data-ttu-id="8232a-118">SoftDeleteFeatureState do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="8232a-118">SoftDeleteFeatureState of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="8232a-119">-Cofreid</span><span class="sxs-lookup"><span data-stu-id="8232a-119">-VaultId</span></span>
<span data-ttu-id="8232a-120">ID do braço do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="8232a-120">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="8232a-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8232a-121">-Confirm</span></span>
<span data-ttu-id="8232a-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8232a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8232a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8232a-123">-WhatIf</span></span>
<span data-ttu-id="8232a-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8232a-124">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="8232a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8232a-125">CommonParameters</span></span>
<span data-ttu-id="8232a-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8232a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8232a-127">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8232a-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8232a-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8232a-128">INPUTS</span></span>

### <span data-ttu-id="8232a-129">System. String</span><span class="sxs-lookup"><span data-stu-id="8232a-129">System.String</span></span>

### <span data-ttu-id="8232a-130">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. VaultSoftDeleteFeatureState</span><span class="sxs-lookup"><span data-stu-id="8232a-130">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.VaultSoftDeleteFeatureState</span></span>

## <span data-ttu-id="8232a-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8232a-131">OUTPUTS</span></span>

### <span data-ttu-id="8232a-132">Microsoft. Azure. Management. Recoveryservices. backup. Models. BackupResourceVaultConfigResource</span><span class="sxs-lookup"><span data-stu-id="8232a-132">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span></span>

## <span data-ttu-id="8232a-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8232a-133">NOTES</span></span>

## <span data-ttu-id="8232a-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8232a-134">RELATED LINKS</span></span>

[<span data-ttu-id="8232a-135">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="8232a-135">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="8232a-136">Get-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="8232a-136">Get-AzRecoveryServicesVaultProperty</span></span>](./Get-AzRecoveryServicesVaultProperty.md)


