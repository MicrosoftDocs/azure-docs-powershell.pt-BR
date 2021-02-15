---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesvaultproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultProperty.md
ms.openlocfilehash: da541e9f019dfb82efc496ce60ab300229e36ac0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114948"
---
# <span data-ttu-id="39a19-101">Get-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="39a19-101">Get-AzRecoveryServicesVaultProperty</span></span>

## <span data-ttu-id="39a19-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="39a19-102">SYNOPSIS</span></span>
<span data-ttu-id="39a19-103">Retorna as propriedades de um Cofre de Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="39a19-103">Returns the properties of a Recovery Services Vault.</span></span>

## <span data-ttu-id="39a19-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="39a19-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesVaultProperty [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="39a19-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="39a19-105">DESCRIPTION</span></span>
<span data-ttu-id="39a19-106">O cmdlet **Get-AzRecoveryServicesVaultProperty** retorna as propriedades de um cofre de serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="39a19-106">The **Get-AzRecoveryServicesVaultProperty** cmdlet returns the properties of a Recovery services vault.</span></span>

## <span data-ttu-id="39a19-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="39a19-107">EXAMPLES</span></span>

### <span data-ttu-id="39a19-108">Exemplo 1: Obter Propriedades de um cofre</span><span class="sxs-lookup"><span data-stu-id="39a19-108">Example 1: Get Properties of a vault</span></span>
```
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $props = Get-AzRecoveryServicesVaultProperty -VaultId $vault.Id
PS C:\> $encryption.encryptionProperties
```

<span data-ttu-id="39a19-109">O primeiro comando obtém um objeto do Cofre e o armazena na variável $vault dados.</span><span class="sxs-lookup"><span data-stu-id="39a19-109">The first command gets a Vault object and then stores it in the $vault variable.</span></span>
<span data-ttu-id="39a19-110">O segundo comando Obtém as Propriedades do Cofre.</span><span class="sxs-lookup"><span data-stu-id="39a19-110">The second command Gets the Vault Properties.</span></span> <span data-ttu-id="39a19-111">Em seguida, acessaremos aspropriedades de criptografia do cofre.</span><span class="sxs-lookup"><span data-stu-id="39a19-111">Next we access the encryptionProperties of the vault.</span></span>

## <span data-ttu-id="39a19-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="39a19-112">PARAMETERS</span></span>

### <span data-ttu-id="39a19-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39a19-113">-DefaultProfile</span></span>
<span data-ttu-id="39a19-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="39a19-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39a19-115">-VaultId</span><span class="sxs-lookup"><span data-stu-id="39a19-115">-VaultId</span></span>
<span data-ttu-id="39a19-116">ID arm do Cofre de Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="39a19-116">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="39a19-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39a19-117">CommonParameters</span></span>
<span data-ttu-id="39a19-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39a19-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39a19-119">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="39a19-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39a19-120">Entradas</span><span class="sxs-lookup"><span data-stu-id="39a19-120">INPUTS</span></span>

### <span data-ttu-id="39a19-121">System.String</span><span class="sxs-lookup"><span data-stu-id="39a19-121">System.String</span></span>

## <span data-ttu-id="39a19-122">Saídas</span><span class="sxs-lookup"><span data-stu-id="39a19-122">OUTPUTS</span></span>

### <span data-ttu-id="39a19-123">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span><span class="sxs-lookup"><span data-stu-id="39a19-123">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span></span>

## <span data-ttu-id="39a19-124">Notas</span><span class="sxs-lookup"><span data-stu-id="39a19-124">NOTES</span></span>

## <span data-ttu-id="39a19-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="39a19-125">RELATED LINKS</span></span>

[<span data-ttu-id="39a19-126">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="39a19-126">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="39a19-127">Set-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="39a19-127">Set-AzRecoveryServicesVaultProperty</span></span>](./Set-AzRecoveryServicesVaultProperty.md)
