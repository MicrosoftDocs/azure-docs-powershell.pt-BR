---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: AFAA1BDF-3F6A-437A-ADC2-C5EBD970F57D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 94e86fdb7f1e995af71e09bdce17754b11819bec
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946564"
---
# <span data-ttu-id="54dc7-101">Get-AzureSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="54dc7-101">Get-AzureSiteRecoveryVaultSettingsFile</span></span>

## <span data-ttu-id="54dc7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="54dc7-102">SYNOPSIS</span></span>
<span data-ttu-id="54dc7-103">Obtém o arquivo de configurações do cofre de recuperação do site.</span><span class="sxs-lookup"><span data-stu-id="54dc7-103">Gets the Site Recovery vault settings file.</span></span>

## <span data-ttu-id="54dc7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="54dc7-104">SYNTAX</span></span>

### <span data-ttu-id="54dc7-105">ByParam (padrão)</span><span class="sxs-lookup"><span data-stu-id="54dc7-105">ByParam (Default)</span></span>
```
Get-AzureSiteRecoveryVaultSettingsFile -Name <String> -Location <String> [-SiteName <String>]
 [-SiteId <String>] [-Path <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="54dc7-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="54dc7-106">ByObject</span></span>
```
Get-AzureSiteRecoveryVaultSettingsFile -Vault <ASRVault> [-Site <ASRSite>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="54dc7-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="54dc7-107">DESCRIPTION</span></span>
<span data-ttu-id="54dc7-108">O cmdlet **Get-AzureSiteRecoveryVaultSettingsFile** Obtém o arquivo de configurações para um cofre do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="54dc7-108">The **Get-AzureSiteRecoveryVaultSettingsFile** cmdlet gets the settings file for an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="54dc7-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="54dc7-109">EXAMPLES</span></span>

### <span data-ttu-id="54dc7-110">Exemplo 1: obter o arquivo de configurações para um cofre</span><span class="sxs-lookup"><span data-stu-id="54dc7-110">Example 1: Get the settings file for a vault</span></span>
```
PS C:\> $Vault = Get-AzureSiteRecoveryVault -Name "ContosoVault"
PS C:\> Get-AzureSiteRecoveryVaultSettingsFile -Vault $Vault
FilePath 
-------- 
C:\Users\ContosoAdmin\ContosoVault_2015-02-02T05-39-23.VaultCredentials
```

<span data-ttu-id="54dc7-111">O primeiro comando obtém o cofre do Azure site Recovery ativo chamado ContosoVault usando o cmdlet **Get-AzureSiteRecoveryVault** .</span><span class="sxs-lookup"><span data-stu-id="54dc7-111">The first command gets the active Azure Site Recovery vault named ContosoVault by using the **Get-AzureSiteRecoveryVault** cmdlet.</span></span>
<span data-ttu-id="54dc7-112">O comando armazena esse cofre na variável $Vault.</span><span class="sxs-lookup"><span data-stu-id="54dc7-112">The command stores that vault in the $Vault variable.</span></span>

<span data-ttu-id="54dc7-113">O segundo comando obtém o arquivo de configurações para o cofre armazenado em $Vault.</span><span class="sxs-lookup"><span data-stu-id="54dc7-113">The second command gets the settings file for the vault stored in $Vault.</span></span>

## <span data-ttu-id="54dc7-114">OS</span><span class="sxs-lookup"><span data-stu-id="54dc7-114">PARAMETERS</span></span>

### <span data-ttu-id="54dc7-115">-Local</span><span class="sxs-lookup"><span data-stu-id="54dc7-115">-Location</span></span>
<span data-ttu-id="54dc7-116">Especifica a localização geográfica à qual o cofre pertence.</span><span class="sxs-lookup"><span data-stu-id="54dc7-116">Specifies the geographical location to which the vault belongs.</span></span>

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54dc7-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="54dc7-117">-Name</span></span>
<span data-ttu-id="54dc7-118">Especifica o nome de um cofre.</span><span class="sxs-lookup"><span data-stu-id="54dc7-118">Specifies the name of a vault.</span></span>

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54dc7-119">-Caminho</span><span class="sxs-lookup"><span data-stu-id="54dc7-119">-Path</span></span>
<span data-ttu-id="54dc7-120">Especifica o caminho do arquivo de configurações do cofre de recuperação do site.</span><span class="sxs-lookup"><span data-stu-id="54dc7-120">Specifies the path of the Site Recovery vault settings file.</span></span>
<span data-ttu-id="54dc7-121">Para armazenar esse arquivo localmente, baixe-o no portal de cofre do site Recovery após concluir a execução do comando.</span><span class="sxs-lookup"><span data-stu-id="54dc7-121">To store this file locally, download it from the Site Recovery vault portal after the command has finished running.</span></span>

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54dc7-122">-Perfil</span><span class="sxs-lookup"><span data-stu-id="54dc7-122">-Profile</span></span>
<span data-ttu-id="54dc7-123">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="54dc7-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="54dc7-124">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="54dc7-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="54dc7-125">-Site</span><span class="sxs-lookup"><span data-stu-id="54dc7-125">-Site</span></span>
<span data-ttu-id="54dc7-126">Especifica um site para o qual obter um arquivo de configurações.</span><span class="sxs-lookup"><span data-stu-id="54dc7-126">Specifies a site for which to get a settings file.</span></span>
<span data-ttu-id="54dc7-127">Para obter um objeto de **site** , use o cmdlet **Get-AzureSiteRecoverySite** .</span><span class="sxs-lookup"><span data-stu-id="54dc7-127">To obtain a **Site** object, use the **Get-AzureSiteRecoverySite** cmdlet.</span></span>

```yaml
Type: ASRSite
Parameter Sets: ByObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54dc7-128">-SiteId</span><span class="sxs-lookup"><span data-stu-id="54dc7-128">-SiteId</span></span>
<span data-ttu-id="54dc7-129">Especifica a ID de um site.</span><span class="sxs-lookup"><span data-stu-id="54dc7-129">Specifies the ID of a site.</span></span>

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54dc7-130">-SiteName</span><span class="sxs-lookup"><span data-stu-id="54dc7-130">-SiteName</span></span>
<span data-ttu-id="54dc7-131">Especifica o nome de um site.</span><span class="sxs-lookup"><span data-stu-id="54dc7-131">Specifies the name of a site.</span></span>

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54dc7-132">-Cofre</span><span class="sxs-lookup"><span data-stu-id="54dc7-132">-Vault</span></span>
<span data-ttu-id="54dc7-133">Especifica o cofre para o site.</span><span class="sxs-lookup"><span data-stu-id="54dc7-133">Specifies the vault for the site.</span></span>

```yaml
Type: ASRVault
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="54dc7-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54dc7-134">CommonParameters</span></span>
<span data-ttu-id="54dc7-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54dc7-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54dc7-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54dc7-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54dc7-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="54dc7-137">INPUTS</span></span>

## <span data-ttu-id="54dc7-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="54dc7-138">OUTPUTS</span></span>

## <span data-ttu-id="54dc7-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="54dc7-139">NOTES</span></span>

## <span data-ttu-id="54dc7-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="54dc7-140">RELATED LINKS</span></span>

[<span data-ttu-id="54dc7-141">Get-AzureSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="54dc7-141">Get-AzureSiteRecoverySite</span></span>](./Get-AzureSiteRecoverySite.md)

[<span data-ttu-id="54dc7-142">Get-AzureSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="54dc7-142">Get-AzureSiteRecoveryVault</span></span>](./Get-AzureSiteRecoveryVault.md)

[<span data-ttu-id="54dc7-143">Get-AzureSiteRecoveryVaultSettings</span><span class="sxs-lookup"><span data-stu-id="54dc7-143">Get-AzureSiteRecoveryVaultSettings</span></span>](./Get-AzureSiteRecoveryVaultSettings.md)

[<span data-ttu-id="54dc7-144">Import-AzureSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="54dc7-144">Import-AzureSiteRecoveryVaultSettingsFile</span></span>](./Import-AzureSiteRecoveryVaultSettingsFile.md)


