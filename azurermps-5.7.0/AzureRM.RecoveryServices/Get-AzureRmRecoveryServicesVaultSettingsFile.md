---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 56074606-28A6-4F91-A56C-4C8A9A31543F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/get-azurermrecoveryservicesvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVaultSettingsFile.md
ms.openlocfilehash: b272f22c0bac37f5318deff50f1f0b56a849ce2d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609500"
---
# <span data-ttu-id="6974b-101">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="6974b-101">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>

## <span data-ttu-id="6974b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6974b-102">SYNOPSIS</span></span>
<span data-ttu-id="6974b-103">Obtém o arquivo de configurações do cofre do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="6974b-103">Gets the Azure Site Recovery vault settings file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6974b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6974b-104">SYNTAX</span></span>

### <span data-ttu-id="6974b-105">ForSite</span><span class="sxs-lookup"><span data-stu-id="6974b-105">ForSite</span></span>
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> -SiteIdentifier <String>
 -SiteFriendlyName <String> [[-Path] <String>] [-SiteRecovery] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6974b-106">ByDefault</span><span class="sxs-lookup"><span data-stu-id="6974b-106">ByDefault</span></span>
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] [-SiteRecovery]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6974b-107">ForBackupVaultType</span><span class="sxs-lookup"><span data-stu-id="6974b-107">ForBackupVaultType</span></span>
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] [-Backup]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6974b-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6974b-108">DESCRIPTION</span></span>
<span data-ttu-id="6974b-109">O cmdlet **Get-AzureRmRecoveryServicesVaultSettingsFile** Obtém o arquivo de configurações para um cofre do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="6974b-109">The **Get-AzureRmRecoveryServicesVaultSettingsFile** cmdlet gets the settings file for an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="6974b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6974b-110">EXAMPLES</span></span>

### <span data-ttu-id="6974b-111">Exemplo 1: registrar um servidor Windows ou um computador do DPM para backup do Azure</span><span class="sxs-lookup"><span data-stu-id="6974b-111">Example 1: Register a Windows Server or DPM machine for Azure Backup</span></span>
```
PS C:\> $Vault01 = Get-AzureRmRecoveryServicesVault -Name "TestVault"
PS C:\> $CredsPath = "C:\Downloads"
PS C:\> $Credsfilename = Get-AzureRmRecoveryServicesVaultSettingsFile -Backup -Vault $Vault01 -Path $CredsPath
```

<span data-ttu-id="6974b-112">O primeiro comando obtém o cofre chamado TestVault e, em seguida, armazena-o na variável $Vault 01.</span><span class="sxs-lookup"><span data-stu-id="6974b-112">The first command gets the vault named TestVault, and then stores it in the $Vault01 variable.</span></span>

<span data-ttu-id="6974b-113">O segundo comando define a variável $CredsPath como C:\Downloads.</span><span class="sxs-lookup"><span data-stu-id="6974b-113">The second command sets the $CredsPath variable to C:\Downloads.</span></span>

<span data-ttu-id="6974b-114">O último comando obtém o arquivo de credenciais do cofre para $Vault 01 usando as credenciais do $CredsPath para o backup do Azure.</span><span class="sxs-lookup"><span data-stu-id="6974b-114">The last command gets the vault credentials file for $Vault01 using the credentials in $CredsPath for Azure Backup.</span></span>

### <span data-ttu-id="6974b-115">Exemplo 2:</span><span class="sxs-lookup"><span data-stu-id="6974b-115">Example 2:</span></span>
```
PS C:\> $Credsfilename = Get-AzureRmRecoveryServicesVaultSettingsFile -SiteIdentifier -Vault $Vault01
```

<span data-ttu-id="6974b-116">O comando obtém o arquivo de credenciais do cofre para $Vault 01 do cofre do tipo de siteRecovery.</span><span class="sxs-lookup"><span data-stu-id="6974b-116">The command gets the vault credentials file for $Vault01 of vault type siteRecovery.</span></span>

### <span data-ttu-id="6974b-117">Exemplo 3: registrar um servidor Windows ou uma máquina do DPM para backup do Azure</span><span class="sxs-lookup"><span data-stu-id="6974b-117">Example 3: Register a Windows Server or DPM machine for Azure Backup</span></span>
```
PS C:\> $Credsfilename = Get-AzureRmRecoveryServicesVaultSettingsFile -SiteIdentifier -Vault $Vault01
```

<span data-ttu-id="6974b-118">O comando obtém o arquivo de credenciais do cofre para $Vault 01.</span><span class="sxs-lookup"><span data-stu-id="6974b-118">The command gets the vault credentials file for $Vault01.</span></span>

## <span data-ttu-id="6974b-119">OS</span><span class="sxs-lookup"><span data-stu-id="6974b-119">PARAMETERS</span></span>

### <span data-ttu-id="6974b-120">-Backup</span><span class="sxs-lookup"><span data-stu-id="6974b-120">-Backup</span></span>
<span data-ttu-id="6974b-121">Indica que o arquivo de credenciais do cofre se aplica ao Azure backup.</span><span class="sxs-lookup"><span data-stu-id="6974b-121">Indicates the vault credentials file is applicable to Azure Backup.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForBackupVaultType
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6974b-122">-Caminho</span><span class="sxs-lookup"><span data-stu-id="6974b-122">-Path</span></span>
<span data-ttu-id="6974b-123">Especifica o caminho para o arquivo de configurações do cofre do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="6974b-123">Specifies the path to the Azure Site Recovery vault settings file.</span></span>
<span data-ttu-id="6974b-124">Você pode baixar esse arquivo do portal de cofre do Azure site Recovery e armazená-lo localmente.</span><span class="sxs-lookup"><span data-stu-id="6974b-124">You can download this file from the Azure Site Recovery vault portal and store it locally.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6974b-125">-SiteFriendlyName</span><span class="sxs-lookup"><span data-stu-id="6974b-125">-SiteFriendlyName</span></span>
<span data-ttu-id="6974b-126">Especifica o nome amigável do site.</span><span class="sxs-lookup"><span data-stu-id="6974b-126">Specifies the site friendly name.</span></span>
<span data-ttu-id="6974b-127">Use esse parâmetro se você estiver baixando as credenciais do cofre para um site do Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="6974b-127">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

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

### <span data-ttu-id="6974b-128">-SiteIdentifier</span><span class="sxs-lookup"><span data-stu-id="6974b-128">-SiteIdentifier</span></span>
<span data-ttu-id="6974b-129">Especifica o identificador do site.</span><span class="sxs-lookup"><span data-stu-id="6974b-129">Specifies the site identifier.</span></span>
<span data-ttu-id="6974b-130">Use esse parâmetro se você estiver baixando as credenciais do cofre para um site do Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="6974b-130">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

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

### <span data-ttu-id="6974b-131">-SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="6974b-131">-SiteRecovery</span></span>
<span data-ttu-id="6974b-132">Indica que o arquivo de credenciais do cofre se aplica ao Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="6974b-132">Indicates the vault credentials file is applicable to Azure Site Recovery.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForSite, ByDefault
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6974b-133">-Cofre</span><span class="sxs-lookup"><span data-stu-id="6974b-133">-Vault</span></span>
<span data-ttu-id="6974b-134">Especifica o objeto do cofre do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="6974b-134">Specifies the Azure Site Recovery vault object.</span></span>

```yaml
Type: ARSVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6974b-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6974b-135">-DefaultProfile</span></span>
<span data-ttu-id="6974b-136">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6974b-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6974b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6974b-137">CommonParameters</span></span>
<span data-ttu-id="6974b-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6974b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6974b-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6974b-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6974b-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6974b-140">INPUTS</span></span>

### <span data-ttu-id="6974b-141">ARSVault</span><span class="sxs-lookup"><span data-stu-id="6974b-141">ARSVault</span></span>
<span data-ttu-id="6974b-142">O parâmetro ' cofre ' aceita o valor do tipo ' ARSVault ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="6974b-142">Parameter 'Vault' accepts value of type 'ARSVault' from the pipeline</span></span>

## <span data-ttu-id="6974b-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6974b-143">OUTPUTS</span></span>

### <span data-ttu-id="6974b-144">Microsoft. Azure. Commands. Recoveryservices. VaultSettingsFilePath</span><span class="sxs-lookup"><span data-stu-id="6974b-144">Microsoft.Azure.Commands.RecoveryServices.VaultSettingsFilePath</span></span>

## <span data-ttu-id="6974b-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6974b-145">NOTES</span></span>

## <span data-ttu-id="6974b-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6974b-146">RELATED LINKS</span></span>

[<span data-ttu-id="6974b-147">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="6974b-147">Get-AzureRmRecoveryServicesVault</span></span>](./Get-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="6974b-148">New-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="6974b-148">New-AzureRmRecoveryServicesVault</span></span>](./New-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="6974b-149">Remove-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="6974b-149">Remove-AzureRmRecoveryServicesVault</span></span>](./Remove-AzureRmRecoveryServicesVault.md)


