---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 305511DC-477F-4A33-8B16-063B39B19ED3
online version: ''
schema: 2.0.0
ms.openlocfilehash: cd96d7dd63791c5ef2e4a8a036949823d5c73313
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946566"
---
# <span data-ttu-id="9c5c4-101">Get-AzureSiteRecoveryVaultSettings</span><span class="sxs-lookup"><span data-stu-id="9c5c4-101">Get-AzureSiteRecoveryVaultSettings</span></span>

## <span data-ttu-id="9c5c4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9c5c4-102">SYNOPSIS</span></span>
<span data-ttu-id="9c5c4-103">Obtém as configurações de um cofre de recuperação de site.</span><span class="sxs-lookup"><span data-stu-id="9c5c4-103">Gets settings for a Site Recovery vault.</span></span>

## <span data-ttu-id="9c5c4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9c5c4-104">SYNTAX</span></span>

```
Get-AzureSiteRecoveryVaultSettings [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9c5c4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9c5c4-105">DESCRIPTION</span></span>
<span data-ttu-id="9c5c4-106">O cmdlet **Get-AzureSiteRecoveryVaultSettings** Obtém configurações relacionadas ao cofre atual do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="9c5c4-106">The **Get-AzureSiteRecoveryVaultSettings** cmdlet gets settings related to the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="9c5c4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9c5c4-107">EXAMPLES</span></span>

### <span data-ttu-id="9c5c4-108">Exemplo 1: obter informações de configuração</span><span class="sxs-lookup"><span data-stu-id="9c5c4-108">Example 1: Get settings information</span></span>
```
PS C:\> Get-AzureSiteRecoveryVaultSettings
ResourceName                                                CloudServiceName
------------                                                ----------------
ContosoVault                                                RecoveryServices-6JP23WE3SKKOM5AFQG2YQAI22MNOWK52QDKWMUP...
```

<span data-ttu-id="9c5c4-109">Este comando obtém informações de configurações para o cofre do Azure site Recovery atual.</span><span class="sxs-lookup"><span data-stu-id="9c5c4-109">This command gets settings information for the current  Azure Site Recovery vault.</span></span>

## <span data-ttu-id="9c5c4-110">OS</span><span class="sxs-lookup"><span data-stu-id="9c5c4-110">PARAMETERS</span></span>

### <span data-ttu-id="9c5c4-111">-Perfil</span><span class="sxs-lookup"><span data-stu-id="9c5c4-111">-Profile</span></span>
<span data-ttu-id="9c5c4-112">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="9c5c4-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9c5c4-113">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="9c5c4-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c5c4-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c5c4-114">CommonParameters</span></span>
<span data-ttu-id="9c5c4-115">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c5c4-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c5c4-116">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c5c4-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c5c4-117">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9c5c4-117">INPUTS</span></span>

## <span data-ttu-id="9c5c4-118">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9c5c4-118">OUTPUTS</span></span>

## <span data-ttu-id="9c5c4-119">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9c5c4-119">NOTES</span></span>

## <span data-ttu-id="9c5c4-120">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9c5c4-120">RELATED LINKS</span></span>

[<span data-ttu-id="9c5c4-121">Get-AzureSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="9c5c4-121">Get-AzureSiteRecoveryVaultSettingsFile</span></span>](./Get-AzureSiteRecoveryVaultSettingsFile.md)

[<span data-ttu-id="9c5c4-122">Import-AzureSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="9c5c4-122">Import-AzureSiteRecoveryVaultSettingsFile</span></span>](./Import-AzureSiteRecoveryVaultSettingsFile.md)


