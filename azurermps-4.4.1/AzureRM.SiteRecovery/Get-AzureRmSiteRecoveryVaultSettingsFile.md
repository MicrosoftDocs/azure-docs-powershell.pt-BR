---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 9595E785-6DBF-433C-83B3-8506A3B49B13
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVaultSettingsFile.md
ms.openlocfilehash: 242dfd46b179d1e7d55613d938eddf5b691da6c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610455"
---
# <span data-ttu-id="1c642-101">Get-AzureRmSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="1c642-101">Get-AzureRmSiteRecoveryVaultSettingsFile</span></span>

## <span data-ttu-id="1c642-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1c642-102">SYNOPSIS</span></span>
<span data-ttu-id="1c642-103">Obtém o arquivo de configurações do cofre de recuperação do site.</span><span class="sxs-lookup"><span data-stu-id="1c642-103">Gets the Site Recovery vault settings file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1c642-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1c642-104">SYNTAX</span></span>

### <span data-ttu-id="1c642-105">ByParam (padrão)</span><span class="sxs-lookup"><span data-stu-id="1c642-105">ByParam (Default)</span></span>
```
Get-AzureRmSiteRecoveryVaultSettingsFile [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c642-106">Assume</span><span class="sxs-lookup"><span data-stu-id="1c642-106">Default</span></span>
```
Get-AzureRmSiteRecoveryVaultSettingsFile -Vault <ASRVault> [-Path <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c642-107">ForSite</span><span class="sxs-lookup"><span data-stu-id="1c642-107">ForSite</span></span>
```
Get-AzureRmSiteRecoveryVaultSettingsFile -Vault <ASRVault> -SiteIdentifier <String> -SiteFriendlyName <String>
 [-Path <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c642-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1c642-108">DESCRIPTION</span></span>
<span data-ttu-id="1c642-109">O cmdlet **Get-AzureRmSiteRecoveryVaultSettingsFile** Obtém o arquivo de configurações para um cofre do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="1c642-109">The **Get-AzureRmSiteRecoveryVaultSettingsFile** cmdlet gets the settings file for an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="1c642-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1c642-110">EXAMPLES</span></span>

## <span data-ttu-id="1c642-111">OS</span><span class="sxs-lookup"><span data-stu-id="1c642-111">PARAMETERS</span></span>

### <span data-ttu-id="1c642-112">-Caminho</span><span class="sxs-lookup"><span data-stu-id="1c642-112">-Path</span></span>
<span data-ttu-id="1c642-113">Especifica o caminho para o arquivo de configurações do cofre de recuperação do site.</span><span class="sxs-lookup"><span data-stu-id="1c642-113">Specifies the path to the Site Recovery vault settings file.</span></span>
<span data-ttu-id="1c642-114">Para armazenar esse arquivo localmente, baixe-o no portal de cofre do site Recovery após a conclusão do comando.</span><span class="sxs-lookup"><span data-stu-id="1c642-114">To store this file locally, download it from the Site Recovery vault portal once the command completes.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, ForSite
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c642-115">-SiteFriendlyName</span><span class="sxs-lookup"><span data-stu-id="1c642-115">-SiteFriendlyName</span></span>
<span data-ttu-id="1c642-116">Especifica o nome amigável do site para o cofre quando o site for um site do Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="1c642-116">Specifies the site friendly name for the vault when the site is a Hyper-V site.</span></span>

```yaml
Type: System.String
Parameter Sets: ForSite
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c642-117">-SiteIdentifier</span><span class="sxs-lookup"><span data-stu-id="1c642-117">-SiteIdentifier</span></span>
<span data-ttu-id="1c642-118">Especifica o identificador de site para o cofre quando o site for um site do Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="1c642-118">Specifies the site identifier for the vault when the site is a Hyper-V site.</span></span>

```yaml
Type: System.String
Parameter Sets: ForSite
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c642-119">-Cofre</span><span class="sxs-lookup"><span data-stu-id="1c642-119">-Vault</span></span>
<span data-ttu-id="1c642-120">Especifica o objeto de cofre para o site.</span><span class="sxs-lookup"><span data-stu-id="1c642-120">Specifies the vault object for the site.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRVault
Parameter Sets: Default, ForSite
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1c642-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c642-121">-DefaultProfile</span></span>
<span data-ttu-id="1c642-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1c642-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1c642-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c642-123">CommonParameters</span></span>
<span data-ttu-id="1c642-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c642-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c642-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c642-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c642-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1c642-126">INPUTS</span></span>

### <span data-ttu-id="1c642-127">ASRVault</span><span class="sxs-lookup"><span data-stu-id="1c642-127">ASRVault</span></span>
<span data-ttu-id="1c642-128">O parâmetro ' cofre ' aceita o valor do tipo ' ASRVault ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="1c642-128">Parameter 'Vault' accepts value of type 'ASRVault' from the pipeline</span></span>

## <span data-ttu-id="1c642-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1c642-129">OUTPUTS</span></span>

### <span data-ttu-id="1c642-130">Microsoft. Azure. Commands. SiteRecovery. VaultSettingsFilePath</span><span class="sxs-lookup"><span data-stu-id="1c642-130">Microsoft.Azure.Commands.SiteRecovery.VaultSettingsFilePath</span></span>

## <span data-ttu-id="1c642-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1c642-131">NOTES</span></span>

## <span data-ttu-id="1c642-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1c642-132">RELATED LINKS</span></span>

[<span data-ttu-id="1c642-133">Import-AzureRmSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="1c642-133">Import-AzureRmSiteRecoveryVaultSettingsFile</span></span>](./Import-AzureRmSiteRecoveryVaultSettingsFile.md)

[<span data-ttu-id="1c642-134">Set-AzureRmSiteRecoveryVaultSettings</span><span class="sxs-lookup"><span data-stu-id="1c642-134">Set-AzureRmSiteRecoveryVaultSettings</span></span>](./Set-AzureRmSiteRecoveryVaultSettings.md)
