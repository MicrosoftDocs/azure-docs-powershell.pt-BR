---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 9595E785-6DBF-433C-83B3-8506A3B49B13
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVaultSettingsFile.md
ms.openlocfilehash: 621e5ac05c5f975ff3878781bcb8c5a1b40c04bf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609913"
---
# <span data-ttu-id="8c90a-101">Get-AzureRmSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="8c90a-101">Get-AzureRmSiteRecoveryVaultSettingsFile</span></span>

## <span data-ttu-id="8c90a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8c90a-102">SYNOPSIS</span></span>
<span data-ttu-id="8c90a-103">Obtém o arquivo de configurações do cofre de recuperação do site.</span><span class="sxs-lookup"><span data-stu-id="8c90a-103">Gets the Site Recovery vault settings file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8c90a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8c90a-104">SYNTAX</span></span>

### <span data-ttu-id="8c90a-105">ByParam (padrão)</span><span class="sxs-lookup"><span data-stu-id="8c90a-105">ByParam (Default)</span></span>
```
Get-AzureRmSiteRecoveryVaultSettingsFile [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c90a-106">Assume</span><span class="sxs-lookup"><span data-stu-id="8c90a-106">Default</span></span>
```
Get-AzureRmSiteRecoveryVaultSettingsFile -Vault <ASRVault> [-Path <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c90a-107">ForSite</span><span class="sxs-lookup"><span data-stu-id="8c90a-107">ForSite</span></span>
```
Get-AzureRmSiteRecoveryVaultSettingsFile -Vault <ASRVault> -SiteIdentifier <String> -SiteFriendlyName <String>
 [-Path <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8c90a-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8c90a-108">DESCRIPTION</span></span>
<span data-ttu-id="8c90a-109">O cmdlet **Get-AzureRmSiteRecoveryVaultSettingsFile** Obtém o arquivo de configurações para um cofre do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="8c90a-109">The **Get-AzureRmSiteRecoveryVaultSettingsFile** cmdlet gets the settings file for an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="8c90a-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8c90a-110">EXAMPLES</span></span>

## <span data-ttu-id="8c90a-111">OS</span><span class="sxs-lookup"><span data-stu-id="8c90a-111">PARAMETERS</span></span>

### <span data-ttu-id="8c90a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c90a-112">-DefaultProfile</span></span>
<span data-ttu-id="8c90a-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8c90a-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c90a-114">-Caminho</span><span class="sxs-lookup"><span data-stu-id="8c90a-114">-Path</span></span>
<span data-ttu-id="8c90a-115">Especifica o caminho para o arquivo de configurações do cofre de recuperação do site.</span><span class="sxs-lookup"><span data-stu-id="8c90a-115">Specifies the path to the Site Recovery vault settings file.</span></span>
<span data-ttu-id="8c90a-116">Para armazenar esse arquivo localmente, baixe-o no portal de cofre do site Recovery após a conclusão do comando.</span><span class="sxs-lookup"><span data-stu-id="8c90a-116">To store this file locally, download it from the Site Recovery vault portal once the command completes.</span></span>

```yaml
Type: String
Parameter Sets: Default, ForSite
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c90a-117">-SiteFriendlyName</span><span class="sxs-lookup"><span data-stu-id="8c90a-117">-SiteFriendlyName</span></span>
<span data-ttu-id="8c90a-118">Especifica o nome amigável do site para o cofre quando o site for um site do Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="8c90a-118">Specifies the site friendly name for the vault when the site is a Hyper-V site.</span></span>

```yaml
Type: String
Parameter Sets: ForSite
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c90a-119">-SiteIdentifier</span><span class="sxs-lookup"><span data-stu-id="8c90a-119">-SiteIdentifier</span></span>
<span data-ttu-id="8c90a-120">Especifica o identificador de site para o cofre quando o site for um site do Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="8c90a-120">Specifies the site identifier for the vault when the site is a Hyper-V site.</span></span>

```yaml
Type: String
Parameter Sets: ForSite
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c90a-121">-Cofre</span><span class="sxs-lookup"><span data-stu-id="8c90a-121">-Vault</span></span>
<span data-ttu-id="8c90a-122">Especifica o objeto de cofre para o site.</span><span class="sxs-lookup"><span data-stu-id="8c90a-122">Specifies the vault object for the site.</span></span>

```yaml
Type: ASRVault
Parameter Sets: Default, ForSite
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8c90a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c90a-123">CommonParameters</span></span>
<span data-ttu-id="8c90a-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c90a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c90a-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c90a-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c90a-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8c90a-126">INPUTS</span></span>

### <span data-ttu-id="8c90a-127">ASRVault</span><span class="sxs-lookup"><span data-stu-id="8c90a-127">ASRVault</span></span>
<span data-ttu-id="8c90a-128">O parâmetro ' cofre ' aceita o valor do tipo ' ASRVault ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="8c90a-128">Parameter 'Vault' accepts value of type 'ASRVault' from the pipeline</span></span>

## <span data-ttu-id="8c90a-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8c90a-129">OUTPUTS</span></span>

### <span data-ttu-id="8c90a-130">Microsoft. Azure. Commands. SiteRecovery. VaultSettingsFilePath</span><span class="sxs-lookup"><span data-stu-id="8c90a-130">Microsoft.Azure.Commands.SiteRecovery.VaultSettingsFilePath</span></span>

## <span data-ttu-id="8c90a-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8c90a-131">NOTES</span></span>

## <span data-ttu-id="8c90a-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8c90a-132">RELATED LINKS</span></span>

[<span data-ttu-id="8c90a-133">Import-AzureRmSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="8c90a-133">Import-AzureRmSiteRecoveryVaultSettingsFile</span></span>](./Import-AzureRmSiteRecoveryVaultSettingsFile.md)

[<span data-ttu-id="8c90a-134">Set-AzureRmSiteRecoveryVaultSettings</span><span class="sxs-lookup"><span data-stu-id="8c90a-134">Set-AzureRmSiteRecoveryVaultSettings</span></span>](./Set-AzureRmSiteRecoveryVaultSettings.md)
