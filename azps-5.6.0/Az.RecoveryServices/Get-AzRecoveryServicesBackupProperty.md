---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProperty.md
ms.openlocfilehash: 2cabaaedbd384237cd8be1469ea5f28cbc1e951f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889412"
---
# <span data-ttu-id="7ddff-101">Get-AzRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="7ddff-101">Get-AzRecoveryServicesBackupProperty</span></span>

## <span data-ttu-id="7ddff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ddff-102">SYNOPSIS</span></span>
<span data-ttu-id="7ddff-103">Obtém propriedades de backup.</span><span class="sxs-lookup"><span data-stu-id="7ddff-103">Gets Backup properties.</span></span>

## <span data-ttu-id="7ddff-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="7ddff-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupProperty -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7ddff-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7ddff-105">DESCRIPTION</span></span>
<span data-ttu-id="7ddff-106">O cmdlet **Get-AzRecoveryServicesBackupProperty** obtém propriedades de backup para um cofre dos Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="7ddff-106">The **Get-AzRecoveryServicesBackupProperty** cmdlet gets backup properties for a Recovery Services vault.</span></span>

## <span data-ttu-id="7ddff-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7ddff-107">EXAMPLES</span></span>

### <span data-ttu-id="7ddff-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7ddff-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesBackupProperty -Vault $vault
```

<span data-ttu-id="7ddff-109">Obter a propriedade do cofre de backup para o cofre.</span><span class="sxs-lookup"><span data-stu-id="7ddff-109">Get the backup vault property for vault.</span></span>

## <span data-ttu-id="7ddff-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="7ddff-110">PARAMETERS</span></span>

### <span data-ttu-id="7ddff-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ddff-111">-DefaultProfile</span></span>
<span data-ttu-id="7ddff-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="7ddff-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ddff-113">-Vault</span><span class="sxs-lookup"><span data-stu-id="7ddff-113">-Vault</span></span>
<span data-ttu-id="7ddff-114">Especifica o nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="7ddff-114">Specifies the name of the vault.</span></span>
<span data-ttu-id="7ddff-115">O cofre deve ser um **objeto AzureRmRecoveryServicesVault.**</span><span class="sxs-lookup"><span data-stu-id="7ddff-115">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="7ddff-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ddff-116">CommonParameters</span></span>
<span data-ttu-id="7ddff-117">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ddff-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ddff-118">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7ddff-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ddff-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7ddff-119">INPUTS</span></span>

### <span data-ttu-id="7ddff-120">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="7ddff-120">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="7ddff-121">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="7ddff-121">OUTPUTS</span></span>

### <span data-ttu-id="7ddff-122">Microsoft.Azure.Commands.RecoveryServices.ASRVaultBackupProperties</span><span class="sxs-lookup"><span data-stu-id="7ddff-122">Microsoft.Azure.Commands.RecoveryServices.ASRVaultBackupProperties</span></span>

## <span data-ttu-id="7ddff-123">NOTES</span><span class="sxs-lookup"><span data-stu-id="7ddff-123">NOTES</span></span>

## <span data-ttu-id="7ddff-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7ddff-124">RELATED LINKS</span></span>
