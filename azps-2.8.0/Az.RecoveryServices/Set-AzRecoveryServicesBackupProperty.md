---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C635D723-0F03-4EF8-9435-24DBE0859899
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesbackupproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProperty.md
ms.openlocfilehash: 6912f54810baeeab795e5f2efca4a51ecafe1c93
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773456"
---
# <span data-ttu-id="727ca-101">Set-AzRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="727ca-101">Set-AzRecoveryServicesBackupProperty</span></span>

## <span data-ttu-id="727ca-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="727ca-102">SYNOPSIS</span></span>
<span data-ttu-id="727ca-103">Define as propriedades do gerenciamento de backup.</span><span class="sxs-lookup"><span data-stu-id="727ca-103">Sets the properties for backup management.</span></span>

## <span data-ttu-id="727ca-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="727ca-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesBackupProperty -Vault <ARSVault>
 [-BackupStorageRedundancy <AzureRmRecoveryServicesBackupStorageRedundancyType>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="727ca-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="727ca-105">DESCRIPTION</span></span>
<span data-ttu-id="727ca-106">O cmdlet **set-AzRecoveryServicesBackupProperty** define as propriedades de armazenamento de backup para um cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="727ca-106">The **Set-AzRecoveryServicesBackupProperty** cmdlet sets backup storage properties for a Recovery Services vault.</span></span>

## <span data-ttu-id="727ca-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="727ca-107">EXAMPLES</span></span>

### <span data-ttu-id="727ca-108">Exemplo 1: definir o armazenamento georedundante para um cofre</span><span class="sxs-lookup"><span data-stu-id="727ca-108">Example 1: Set GeoRedundant storage for a vault</span></span>
```
PS C:\> $Vault01 = Get-AzRecoveryServicesVault -Name "TestVault"
PS C:\> Set-AzRecoveryServicesBackupProperty -Vault $Vault01 -BackupStorageRedundancy GeoRedundant
```

<span data-ttu-id="727ca-109">O primeiro comando obtém o cofre chamado TestVault e, em seguida, armazena-o na variável $Vault 01.</span><span class="sxs-lookup"><span data-stu-id="727ca-109">The first command gets the vault named TestVault, and then stores it in the $Vault01 variable.</span></span>
<span data-ttu-id="727ca-110">O segundo comando define a redundância de armazenamento de backup para $Vault 01 a georedundante.</span><span class="sxs-lookup"><span data-stu-id="727ca-110">The second command sets the backup storage redundancy for $Vault01 to GeoRedundant.</span></span>

## <span data-ttu-id="727ca-111">OS</span><span class="sxs-lookup"><span data-stu-id="727ca-111">PARAMETERS</span></span>

### <span data-ttu-id="727ca-112">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="727ca-112">-BackupStorageRedundancy</span></span>
<span data-ttu-id="727ca-113">Especifica o tipo de redundância do armazenamento de backup.</span><span class="sxs-lookup"><span data-stu-id="727ca-113">Specifies the backup storage redundancy type.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.AzureRmRecoveryServicesBackupStorageRedundancyType]
Parameter Sets: (All)
Aliases:
Accepted values: GeoRedundant, LocallyRedundant

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="727ca-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="727ca-114">-DefaultProfile</span></span>
<span data-ttu-id="727ca-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="727ca-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="727ca-116">-Cofre</span><span class="sxs-lookup"><span data-stu-id="727ca-116">-Vault</span></span>
<span data-ttu-id="727ca-117">Especifica o nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="727ca-117">Specifies the name of the vault.</span></span>
<span data-ttu-id="727ca-118">O cofre deve ser um objeto **AzureRmRecoveryServicesVault** .</span><span class="sxs-lookup"><span data-stu-id="727ca-118">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="727ca-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="727ca-119">-Confirm</span></span>
<span data-ttu-id="727ca-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="727ca-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="727ca-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="727ca-121">-WhatIf</span></span>
<span data-ttu-id="727ca-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="727ca-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="727ca-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="727ca-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="727ca-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="727ca-124">CommonParameters</span></span>
<span data-ttu-id="727ca-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="727ca-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="727ca-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="727ca-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="727ca-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="727ca-127">INPUTS</span></span>

### <span data-ttu-id="727ca-128">Microsoft. Azure. Commands. Recoveryservices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="727ca-128">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="727ca-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="727ca-129">OUTPUTS</span></span>

### <span data-ttu-id="727ca-130">System. void</span><span class="sxs-lookup"><span data-stu-id="727ca-130">System.Void</span></span>

## <span data-ttu-id="727ca-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="727ca-131">NOTES</span></span>

## <span data-ttu-id="727ca-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="727ca-132">RELATED LINKS</span></span>

[<span data-ttu-id="727ca-133">Get-AzRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="727ca-133">Get-AzRecoveryServicesBackupProperty</span></span>](./Get-AzRecoveryServicesBackupProperty.md)

[<span data-ttu-id="727ca-134">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="727ca-134">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

