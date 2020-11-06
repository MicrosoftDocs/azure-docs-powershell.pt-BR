---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/get-azurermrecoveryservicesbackupproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesBackupProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesBackupProperty.md
ms.openlocfilehash: d900da862572c0e3a51f288a7e6bec948f7aeba4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429392"
---
# <span data-ttu-id="84278-101">Get-AzureRmRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="84278-101">Get-AzureRmRecoveryServicesBackupProperty</span></span>

## <span data-ttu-id="84278-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="84278-102">SYNOPSIS</span></span>
<span data-ttu-id="84278-103">Obtém Propriedades de backup.</span><span class="sxs-lookup"><span data-stu-id="84278-103">Gets Backup properties.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="84278-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="84278-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupProperty -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="84278-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="84278-105">DESCRIPTION</span></span>
<span data-ttu-id="84278-106">O cmdlet **Get-AzureRmRecoveryServicesBackupProperty** Obtém Propriedades de backup para um cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="84278-106">The **Get-AzureRmRecoveryServicesBackupProperty** cmdlet gets backup properties for a Recovery Services vault.</span></span>

## <span data-ttu-id="84278-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="84278-107">EXAMPLES</span></span>

### <span data-ttu-id="84278-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="84278-108">Example 1</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesBackupProperty -Vault $vault
```

<span data-ttu-id="84278-109">Obter a propriedade de cofre de backup para o cofre.</span><span class="sxs-lookup"><span data-stu-id="84278-109">Get the backup vault property for vault.</span></span>

## <span data-ttu-id="84278-110">OS</span><span class="sxs-lookup"><span data-stu-id="84278-110">PARAMETERS</span></span>

### <span data-ttu-id="84278-111">-Cofre</span><span class="sxs-lookup"><span data-stu-id="84278-111">-Vault</span></span>
<span data-ttu-id="84278-112">Especifica o nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="84278-112">Specifies the name of the vault.</span></span>
<span data-ttu-id="84278-113">O cofre deve ser um objeto **AzureRmRecoveryServicesVault** .</span><span class="sxs-lookup"><span data-stu-id="84278-113">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="84278-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84278-114">-DefaultProfile</span></span>
<span data-ttu-id="84278-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="84278-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84278-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84278-116">CommonParameters</span></span>
<span data-ttu-id="84278-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84278-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84278-118">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84278-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84278-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="84278-119">INPUTS</span></span>

### <span data-ttu-id="84278-120">Microsoft. Azure. Commands. Recoveryservices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="84278-120">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>
<span data-ttu-id="84278-121">Parâmetros: cofre (ByValue)</span><span class="sxs-lookup"><span data-stu-id="84278-121">Parameters: Vault (ByValue)</span></span>

## <span data-ttu-id="84278-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="84278-122">OUTPUTS</span></span>

### <span data-ttu-id="84278-123">Microsoft. Azure. Commands. Recoveryservices. ASRVaultBackupProperties</span><span class="sxs-lookup"><span data-stu-id="84278-123">Microsoft.Azure.Commands.RecoveryServices.ASRVaultBackupProperties</span></span>

## <span data-ttu-id="84278-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="84278-124">NOTES</span></span>

## <span data-ttu-id="84278-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="84278-125">RELATED LINKS</span></span>
