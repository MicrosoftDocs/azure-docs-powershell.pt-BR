---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProperty.md
ms.openlocfilehash: efe463bab4195dfb09692f76d0e02e3aeaa59344
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113374"
---
# <span data-ttu-id="6de75-101">Get-AzRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="6de75-101">Get-AzRecoveryServicesBackupProperty</span></span>

## <span data-ttu-id="6de75-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6de75-102">SYNOPSIS</span></span>
<span data-ttu-id="6de75-103">Obtém propriedades de Backup.</span><span class="sxs-lookup"><span data-stu-id="6de75-103">Gets Backup properties.</span></span>

## <span data-ttu-id="6de75-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6de75-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupProperty -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6de75-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="6de75-105">DESCRIPTION</span></span>
<span data-ttu-id="6de75-106">O cmdlet **Get-AzRecoveryServicesBackupProperty** obtém propriedades de backup para um cofre do Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="6de75-106">The **Get-AzRecoveryServicesBackupProperty** cmdlet gets backup properties for a Recovery Services vault.</span></span>

## <span data-ttu-id="6de75-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6de75-107">EXAMPLES</span></span>

### <span data-ttu-id="6de75-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6de75-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesBackupProperty -Vault $vault
```

<span data-ttu-id="6de75-109">Obter a propriedade do cofre de backup para o cofre.</span><span class="sxs-lookup"><span data-stu-id="6de75-109">Get the backup vault property for vault.</span></span>

## <span data-ttu-id="6de75-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6de75-110">PARAMETERS</span></span>

### <span data-ttu-id="6de75-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6de75-111">-DefaultProfile</span></span>
<span data-ttu-id="6de75-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="6de75-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6de75-113">-Cofre</span><span class="sxs-lookup"><span data-stu-id="6de75-113">-Vault</span></span>
<span data-ttu-id="6de75-114">Especifica o nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="6de75-114">Specifies the name of the vault.</span></span>
<span data-ttu-id="6de75-115">O cofre deve ser um **objeto AzureRmRecoveryServicesVault.**</span><span class="sxs-lookup"><span data-stu-id="6de75-115">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="6de75-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6de75-116">CommonParameters</span></span>
<span data-ttu-id="6de75-117">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6de75-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6de75-118">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6de75-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6de75-119">Entradas</span><span class="sxs-lookup"><span data-stu-id="6de75-119">INPUTS</span></span>

### <span data-ttu-id="6de75-120">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="6de75-120">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="6de75-121">Saídas</span><span class="sxs-lookup"><span data-stu-id="6de75-121">OUTPUTS</span></span>

### <span data-ttu-id="6de75-122">Microsoft.Azure.Commands.RecoveryServices.ASRVaultBackupProperties</span><span class="sxs-lookup"><span data-stu-id="6de75-122">Microsoft.Azure.Commands.RecoveryServices.ASRVaultBackupProperties</span></span>

## <span data-ttu-id="6de75-123">Notas</span><span class="sxs-lookup"><span data-stu-id="6de75-123">NOTES</span></span>

## <span data-ttu-id="6de75-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6de75-124">RELATED LINKS</span></span>
