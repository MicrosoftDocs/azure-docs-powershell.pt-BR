---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProperty.md
ms.openlocfilehash: efe463bab4195dfb09692f76d0e02e3aeaa59344
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98428055"
---
# <span data-ttu-id="098f6-101">Get-AzRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="098f6-101">Get-AzRecoveryServicesBackupProperty</span></span>

## <span data-ttu-id="098f6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="098f6-102">SYNOPSIS</span></span>
<span data-ttu-id="098f6-103">Obtém Propriedades de backup.</span><span class="sxs-lookup"><span data-stu-id="098f6-103">Gets Backup properties.</span></span>

## <span data-ttu-id="098f6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="098f6-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupProperty -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="098f6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="098f6-105">DESCRIPTION</span></span>
<span data-ttu-id="098f6-106">O cmdlet **Get-AzRecoveryServicesBackupProperty** Obtém Propriedades de backup para um cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="098f6-106">The **Get-AzRecoveryServicesBackupProperty** cmdlet gets backup properties for a Recovery Services vault.</span></span>

## <span data-ttu-id="098f6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="098f6-107">EXAMPLES</span></span>

### <span data-ttu-id="098f6-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="098f6-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesBackupProperty -Vault $vault
```

<span data-ttu-id="098f6-109">Obter a propriedade de cofre de backup para o cofre.</span><span class="sxs-lookup"><span data-stu-id="098f6-109">Get the backup vault property for vault.</span></span>

## <span data-ttu-id="098f6-110">OS</span><span class="sxs-lookup"><span data-stu-id="098f6-110">PARAMETERS</span></span>

### <span data-ttu-id="098f6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="098f6-111">-DefaultProfile</span></span>
<span data-ttu-id="098f6-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="098f6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="098f6-113">-Cofre</span><span class="sxs-lookup"><span data-stu-id="098f6-113">-Vault</span></span>
<span data-ttu-id="098f6-114">Especifica o nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="098f6-114">Specifies the name of the vault.</span></span>
<span data-ttu-id="098f6-115">O cofre deve ser um objeto **AzureRmRecoveryServicesVault** .</span><span class="sxs-lookup"><span data-stu-id="098f6-115">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="098f6-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="098f6-116">CommonParameters</span></span>
<span data-ttu-id="098f6-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="098f6-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="098f6-118">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="098f6-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="098f6-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="098f6-119">INPUTS</span></span>

### <span data-ttu-id="098f6-120">Microsoft. Azure. Commands. Recoveryservices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="098f6-120">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="098f6-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="098f6-121">OUTPUTS</span></span>

### <span data-ttu-id="098f6-122">Microsoft. Azure. Commands. Recoveryservices. ASRVaultBackupProperties</span><span class="sxs-lookup"><span data-stu-id="098f6-122">Microsoft.Azure.Commands.RecoveryServices.ASRVaultBackupProperties</span></span>

## <span data-ttu-id="098f6-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="098f6-123">NOTES</span></span>

## <span data-ttu-id="098f6-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="098f6-124">RELATED LINKS</span></span>
