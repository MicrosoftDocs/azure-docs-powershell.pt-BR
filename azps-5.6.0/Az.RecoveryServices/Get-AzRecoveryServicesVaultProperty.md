---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesvaultproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultProperty.md
ms.openlocfilehash: 4e0b74ead08a3b944e66b46a6fee0fb71976b223
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888091"
---
# <span data-ttu-id="d14e4-101">Get-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="d14e4-101">Get-AzRecoveryServicesVaultProperty</span></span>

## <span data-ttu-id="d14e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d14e4-102">SYNOPSIS</span></span>
<span data-ttu-id="d14e4-103">Retorna as propriedades de um Cofre de Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="d14e4-103">Returns the properties of a Recovery Services Vault.</span></span>

## <span data-ttu-id="d14e4-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d14e4-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesVaultProperty [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d14e4-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d14e4-105">DESCRIPTION</span></span>
<span data-ttu-id="d14e4-106">O cmdlet **Get-AzRecoveryServicesVaultProperty** retorna as propriedades de um cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="d14e4-106">The **Get-AzRecoveryServicesVaultProperty** cmdlet returns the properties of a Recovery services vault.</span></span>

## <span data-ttu-id="d14e4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d14e4-107">EXAMPLES</span></span>

### <span data-ttu-id="d14e4-108">Exemplo 1: Obter propriedades de um cofre</span><span class="sxs-lookup"><span data-stu-id="d14e4-108">Example 1: Get Properties of a vault</span></span>
```
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $props = Get-AzRecoveryServicesVaultProperty -VaultId $vault.Id
PS C:\> $encryption.encryptionProperties
```

<span data-ttu-id="d14e4-109">O primeiro comando obtém um objeto Vault e o armazena na $vault variável.</span><span class="sxs-lookup"><span data-stu-id="d14e4-109">The first command gets a Vault object and then stores it in the $vault variable.</span></span>
<span data-ttu-id="d14e4-110">O segundo comando Obtém as Propriedades do Cofre.</span><span class="sxs-lookup"><span data-stu-id="d14e4-110">The second command Gets the Vault Properties.</span></span> <span data-ttu-id="d14e4-111">Em seguida, acessamos as encryptionProperties do cofre.</span><span class="sxs-lookup"><span data-stu-id="d14e4-111">Next we access the encryptionProperties of the vault.</span></span>

## <span data-ttu-id="d14e4-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d14e4-112">PARAMETERS</span></span>

### <span data-ttu-id="d14e4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d14e4-113">-DefaultProfile</span></span>
<span data-ttu-id="d14e4-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="d14e4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d14e4-115">-VaultId</span><span class="sxs-lookup"><span data-stu-id="d14e4-115">-VaultId</span></span>
<span data-ttu-id="d14e4-116">ARM ID do Cofre de Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="d14e4-116">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="d14e4-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d14e4-117">CommonParameters</span></span>
<span data-ttu-id="d14e4-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d14e4-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d14e4-119">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d14e4-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d14e4-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d14e4-120">INPUTS</span></span>

### <span data-ttu-id="d14e4-121">System.String</span><span class="sxs-lookup"><span data-stu-id="d14e4-121">System.String</span></span>

## <span data-ttu-id="d14e4-122">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d14e4-122">OUTPUTS</span></span>

### <span data-ttu-id="d14e4-123">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span><span class="sxs-lookup"><span data-stu-id="d14e4-123">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span></span>

## <span data-ttu-id="d14e4-124">NOTES</span><span class="sxs-lookup"><span data-stu-id="d14e4-124">NOTES</span></span>

## <span data-ttu-id="d14e4-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d14e4-125">RELATED LINKS</span></span>

[<span data-ttu-id="d14e4-126">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="d14e4-126">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="d14e4-127">Set-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="d14e4-127">Set-AzRecoveryServicesVaultProperty</span></span>](./Set-AzRecoveryServicesVaultProperty.md)
