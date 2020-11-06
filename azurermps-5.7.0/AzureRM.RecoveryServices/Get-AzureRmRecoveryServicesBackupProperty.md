---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/get-azurermrecoveryservicesbackupproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesBackupProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesBackupProperty.md
ms.openlocfilehash: 19e443a4e7bca12a988e3a339fe9d568d81431b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432924"
---
# <span data-ttu-id="8c38f-101">Get-AzureRmRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="8c38f-101">Get-AzureRmRecoveryServicesBackupProperty</span></span>

## <span data-ttu-id="8c38f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8c38f-102">SYNOPSIS</span></span>
<span data-ttu-id="8c38f-103">Obtém Propriedades de backup.</span><span class="sxs-lookup"><span data-stu-id="8c38f-103">Gets Backup properties.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8c38f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8c38f-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupProperty -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8c38f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8c38f-105">DESCRIPTION</span></span>
<span data-ttu-id="8c38f-106">O cmdlet **Get-AzureRmRecoveryServicesBackupProperty** Obtém Propriedades de backup para um cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="8c38f-106">The **Get-AzureRmRecoveryServicesBackupProperty** cmdlet gets backup properties for a Recovery Services vault.</span></span>

## <span data-ttu-id="8c38f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8c38f-107">EXAMPLES</span></span>

### <span data-ttu-id="8c38f-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8c38f-108">Example 1</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesBackupProperty -Vault $vault
```

<span data-ttu-id="8c38f-109">Obter a propriedade de cofre de backup para o cofre.</span><span class="sxs-lookup"><span data-stu-id="8c38f-109">Get the backup vault property for vault.</span></span>

## <span data-ttu-id="8c38f-110">OS</span><span class="sxs-lookup"><span data-stu-id="8c38f-110">PARAMETERS</span></span>

### <span data-ttu-id="8c38f-111">-Cofre</span><span class="sxs-lookup"><span data-stu-id="8c38f-111">-Vault</span></span>
<span data-ttu-id="8c38f-112">Especifica o nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="8c38f-112">Specifies the name of the vault.</span></span>
<span data-ttu-id="8c38f-113">O cofre deve ser um objeto **AzureRmRecoveryServicesVault** .</span><span class="sxs-lookup"><span data-stu-id="8c38f-113">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

```yaml
Type: ARSVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8c38f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c38f-114">-DefaultProfile</span></span>
<span data-ttu-id="8c38f-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8c38f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c38f-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c38f-116">CommonParameters</span></span>
<span data-ttu-id="8c38f-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c38f-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c38f-118">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c38f-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c38f-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8c38f-119">INPUTS</span></span>

### <span data-ttu-id="8c38f-120">Microsoft. Azure. Commands. Recoveryservices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="8c38f-120">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="8c38f-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8c38f-121">OUTPUTS</span></span>

### <span data-ttu-id="8c38f-122">Microsoft. Azure. Commands. Recoveryservices. ASRVaultBackupProperties</span><span class="sxs-lookup"><span data-stu-id="8c38f-122">Microsoft.Azure.Commands.RecoveryServices.ASRVaultBackupProperties</span></span>

## <span data-ttu-id="8c38f-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8c38f-123">NOTES</span></span>

## <span data-ttu-id="8c38f-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8c38f-124">RELATED LINKS</span></span>
