---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesBackupProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesBackupProperty.md
ms.openlocfilehash: 3e93df0adfe1e1bc10d5ea74dd189bee60595824
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609584"
---
# <span data-ttu-id="9036a-101">Get-AzureRmRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="9036a-101">Get-AzureRmRecoveryServicesBackupProperty</span></span>

## <span data-ttu-id="9036a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9036a-102">SYNOPSIS</span></span>
<span data-ttu-id="9036a-103">Obtém Propriedades de backup.</span><span class="sxs-lookup"><span data-stu-id="9036a-103">Gets Backup properties.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9036a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9036a-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupProperty -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9036a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9036a-105">DESCRIPTION</span></span>
<span data-ttu-id="9036a-106">O cmdlet **Get-AzureRmRecoveryServicesBackupProperty** Obtém Propriedades de backup para um cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="9036a-106">The **Get-AzureRmRecoveryServicesBackupProperty** cmdlet gets backup properties for a Recovery Services vault.</span></span>

## <span data-ttu-id="9036a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9036a-107">EXAMPLES</span></span>

## <span data-ttu-id="9036a-108">OS</span><span class="sxs-lookup"><span data-stu-id="9036a-108">PARAMETERS</span></span>

### <span data-ttu-id="9036a-109">-Cofre</span><span class="sxs-lookup"><span data-stu-id="9036a-109">-Vault</span></span>
<span data-ttu-id="9036a-110">Especifica o nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="9036a-110">Specifies the name of the vault.</span></span>
<span data-ttu-id="9036a-111">O cofre deve ser um objeto **AzureRmRecoveryServicesVault** .</span><span class="sxs-lookup"><span data-stu-id="9036a-111">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="9036a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9036a-112">-DefaultProfile</span></span>
<span data-ttu-id="9036a-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9036a-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9036a-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9036a-114">CommonParameters</span></span>
<span data-ttu-id="9036a-115">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9036a-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9036a-116">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9036a-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9036a-117">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9036a-117">INPUTS</span></span>

### <span data-ttu-id="9036a-118">Microsoft. Azure. Commands. Recoveryservices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="9036a-118">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="9036a-119">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9036a-119">OUTPUTS</span></span>

### <span data-ttu-id="9036a-120">Microsoft. Azure. Commands. Recoveryservices. ASRVaultBackupProperties</span><span class="sxs-lookup"><span data-stu-id="9036a-120">Microsoft.Azure.Commands.RecoveryServices.ASRVaultBackupProperties</span></span>

## <span data-ttu-id="9036a-121">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9036a-121">NOTES</span></span>

## <span data-ttu-id="9036a-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9036a-122">RELATED LINKS</span></span>

