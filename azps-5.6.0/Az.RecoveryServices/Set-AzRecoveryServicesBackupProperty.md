---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C635D723-0F03-4EF8-9435-24DBE0859899
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/set-azrecoveryservicesbackupproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProperty.md
ms.openlocfilehash: 5e66fc57f6ee9daffde27226bc0321f415cc10d4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891296"
---
# <span data-ttu-id="211c8-101">Set-AzRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="211c8-101">Set-AzRecoveryServicesBackupProperty</span></span>

## <span data-ttu-id="211c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="211c8-102">SYNOPSIS</span></span>
<span data-ttu-id="211c8-103">Define as propriedades para gerenciamento de backup.</span><span class="sxs-lookup"><span data-stu-id="211c8-103">Sets the properties for backup management.</span></span>

## <span data-ttu-id="211c8-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="211c8-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesBackupProperty -Vault <ARSVault>  [-BackupStorageRedundancy <AzureRmRecoveryServicesBackupStorageRedundancyType>]
 [-EnableCrossRegionRestore] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="211c8-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="211c8-105">DESCRIPTION</span></span>
<span data-ttu-id="211c8-106">O cmdlet **Set-AzRecoveryServicesBackupProperty** define propriedades de armazenamento de backup para um cofre dos Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="211c8-106">The **Set-AzRecoveryServicesBackupProperty** cmdlet sets backup storage properties for a Recovery Services vault.</span></span>

## <span data-ttu-id="211c8-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="211c8-107">EXAMPLES</span></span>

### <span data-ttu-id="211c8-108">Exemplo 1: Definir o armazenamento GeoRedundant para um cofre</span><span class="sxs-lookup"><span data-stu-id="211c8-108">Example 1: Set GeoRedundant storage for a vault</span></span>
```
PS C:\> $Vault01 = Get-AzRecoveryServicesVault -Name "TestVault"
PS C:\> Set-AzRecoveryServicesBackupProperty -Vault $Vault01 -BackupStorageRedundancy GeoRedundant
```

<span data-ttu-id="211c8-109">O primeiro comando obtém o cofre chamado TestVault e o armazena na variável $Vault 01.</span><span class="sxs-lookup"><span data-stu-id="211c8-109">The first command gets the vault named TestVault, and then stores it in the $Vault01 variable.</span></span>
<span data-ttu-id="211c8-110">O segundo comando define a redundância de armazenamento de backup para $Vault 01 como GeoRedundant.</span><span class="sxs-lookup"><span data-stu-id="211c8-110">The second command sets the backup storage redundancy for $Vault01 to GeoRedundant.</span></span>

## <span data-ttu-id="211c8-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="211c8-111">PARAMETERS</span></span>

### <span data-ttu-id="211c8-112">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="211c8-112">-BackupStorageRedundancy</span></span>
<span data-ttu-id="211c8-113">Especifica o tipo de redundância de armazenamento de backup.</span><span class="sxs-lookup"><span data-stu-id="211c8-113">Specifies the backup storage redundancy type.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.AzureRmRecoveryServicesBackupStorageRedundancyType]
Parameter Sets: (All)
Aliases:
Accepted values: GeoRedundant, ZoneRedundant, LocallyRedundant

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="211c8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="211c8-114">-DefaultProfile</span></span>
<span data-ttu-id="211c8-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="211c8-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="211c8-116">-Vault</span><span class="sxs-lookup"><span data-stu-id="211c8-116">-Vault</span></span>
<span data-ttu-id="211c8-117">Especifica o nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="211c8-117">Specifies the name of the vault.</span></span>
<span data-ttu-id="211c8-118">O cofre deve ser um **objeto AzureRmRecoveryServicesVault.**</span><span class="sxs-lookup"><span data-stu-id="211c8-118">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="211c8-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="211c8-119">-Confirm</span></span>
<span data-ttu-id="211c8-120">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="211c8-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="211c8-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="211c8-121">-WhatIf</span></span>
<span data-ttu-id="211c8-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="211c8-122">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="211c8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="211c8-123">CommonParameters</span></span>
<span data-ttu-id="211c8-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="211c8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="211c8-125">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="211c8-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="211c8-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="211c8-126">INPUTS</span></span>

### <span data-ttu-id="211c8-127">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="211c8-127">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="211c8-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="211c8-128">OUTPUTS</span></span>

### <span data-ttu-id="211c8-129">System.Void</span><span class="sxs-lookup"><span data-stu-id="211c8-129">System.Void</span></span>

## <span data-ttu-id="211c8-130">NOTES</span><span class="sxs-lookup"><span data-stu-id="211c8-130">NOTES</span></span>

## <span data-ttu-id="211c8-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="211c8-131">RELATED LINKS</span></span>

[<span data-ttu-id="211c8-132">Get-AzRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="211c8-132">Get-AzRecoveryServicesBackupProperty</span></span>](./Get-AzRecoveryServicesBackupProperty.md)

[<span data-ttu-id="211c8-133">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="211c8-133">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)


