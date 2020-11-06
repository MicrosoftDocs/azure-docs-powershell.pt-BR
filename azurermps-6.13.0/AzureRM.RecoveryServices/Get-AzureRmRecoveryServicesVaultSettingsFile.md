---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 56074606-28A6-4F91-A56C-4C8A9A31543F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/get-azurermrecoveryservicesvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVaultSettingsFile.md
ms.openlocfilehash: a0572e73d270a37b3c705018a38b4a88fe88d1e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440299"
---
# <span data-ttu-id="8f568-101">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="8f568-101">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>

## <span data-ttu-id="8f568-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8f568-102">SYNOPSIS</span></span>
<span data-ttu-id="8f568-103">Obtém o arquivo de configurações do cofre do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="8f568-103">Gets the Azure Site Recovery vault settings file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f568-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8f568-104">SYNTAX</span></span>

### <span data-ttu-id="8f568-105">ForSite</span><span class="sxs-lookup"><span data-stu-id="8f568-105">ForSite</span></span>
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> -SiteIdentifier <String>
 -SiteFriendlyName <String> [[-Path] <String>] [-SiteRecovery] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8f568-106">ByDefault</span><span class="sxs-lookup"><span data-stu-id="8f568-106">ByDefault</span></span>
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] [-SiteRecovery]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f568-107">ForBackupVaultType</span><span class="sxs-lookup"><span data-stu-id="8f568-107">ForBackupVaultType</span></span>
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] [-Backup]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8f568-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8f568-108">DESCRIPTION</span></span>
<span data-ttu-id="8f568-109">O cmdlet **Get-AzureRmRecoveryServicesVaultSettingsFile** Obtém o arquivo de configurações para um cofre do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="8f568-109">The **Get-AzureRmRecoveryServicesVaultSettingsFile** cmdlet gets the settings file for an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="8f568-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8f568-110">EXAMPLES</span></span>

### <span data-ttu-id="8f568-111">Exemplo 1: registrar um servidor Windows ou um computador do DPM para backup do Azure</span><span class="sxs-lookup"><span data-stu-id="8f568-111">Example 1: Register a Windows Server or DPM machine for Azure Backup</span></span>
```
PS C:\> $Vault01 = Get-AzureRmRecoveryServicesVault -Name "TestVault"
PS C:\> $CredsPath = "C:\Downloads"
PS C:\> $Credsfilename = Get-AzureRmRecoveryServicesVaultSettingsFile -Backup -Vault $Vault01 -Path $CredsPath
```

<span data-ttu-id="8f568-112">O primeiro comando obtém o cofre chamado TestVault e, em seguida, armazena-o na variável $Vault 01.</span><span class="sxs-lookup"><span data-stu-id="8f568-112">The first command gets the vault named TestVault, and then stores it in the $Vault01 variable.</span></span>
<span data-ttu-id="8f568-113">O segundo comando define a variável $CredsPath como C:\Downloads.</span><span class="sxs-lookup"><span data-stu-id="8f568-113">The second command sets the $CredsPath variable to C:\Downloads.</span></span>
<span data-ttu-id="8f568-114">O último comando obtém o arquivo de credenciais do cofre para $Vault 01 usando as credenciais do $CredsPath para o backup do Azure.</span><span class="sxs-lookup"><span data-stu-id="8f568-114">The last command gets the vault credentials file for $Vault01 using the credentials in $CredsPath for Azure Backup.</span></span>

### <span data-ttu-id="8f568-115">Exemplo 2:</span><span class="sxs-lookup"><span data-stu-id="8f568-115">Example 2:</span></span>
```
PS C:\> $Credsfilename = Get-AzureRmRecoveryServicesVaultSettingsFile -SiteIdentifier -Vault $Vault01
```

<span data-ttu-id="8f568-116">O comando obtém o arquivo de credenciais do cofre para $Vault 01 do cofre do tipo de siteRecovery.</span><span class="sxs-lookup"><span data-stu-id="8f568-116">The command gets the vault credentials file for $Vault01 of vault type siteRecovery.</span></span>

### <span data-ttu-id="8f568-117">Exemplo 3: registrar um servidor Windows ou uma máquina do DPM para backup do Azure</span><span class="sxs-lookup"><span data-stu-id="8f568-117">Example 3: Register a Windows Server or DPM machine for Azure Backup</span></span>
```
PS C:\> $Credsfilename = Get-AzureRmRecoveryServicesVaultSettingsFile -SiteIdentifier -Vault $Vault01
```

<span data-ttu-id="8f568-118">O comando obtém o arquivo de credenciais do cofre para $Vault 01.</span><span class="sxs-lookup"><span data-stu-id="8f568-118">The command gets the vault credentials file for $Vault01.</span></span>

## <span data-ttu-id="8f568-119">OS</span><span class="sxs-lookup"><span data-stu-id="8f568-119">PARAMETERS</span></span>

### <span data-ttu-id="8f568-120">-Backup</span><span class="sxs-lookup"><span data-stu-id="8f568-120">-Backup</span></span>
<span data-ttu-id="8f568-121">Indica que o arquivo de credenciais do cofre se aplica ao Azure backup.</span><span class="sxs-lookup"><span data-stu-id="8f568-121">Indicates the vault credentials file is applicable to Azure Backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForBackupVaultType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f568-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f568-122">-DefaultProfile</span></span>
<span data-ttu-id="8f568-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8f568-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f568-124">-Caminho</span><span class="sxs-lookup"><span data-stu-id="8f568-124">-Path</span></span>
<span data-ttu-id="8f568-125">Especifica o caminho para o arquivo de configurações do cofre do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="8f568-125">Specifies the path to the Azure Site Recovery vault settings file.</span></span>
<span data-ttu-id="8f568-126">Você pode baixar esse arquivo do portal de cofre do Azure site Recovery e armazená-lo localmente.</span><span class="sxs-lookup"><span data-stu-id="8f568-126">You can download this file from the Azure Site Recovery vault portal and store it locally.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f568-127">-SiteFriendlyName</span><span class="sxs-lookup"><span data-stu-id="8f568-127">-SiteFriendlyName</span></span>
<span data-ttu-id="8f568-128">Especifica o nome amigável do site.</span><span class="sxs-lookup"><span data-stu-id="8f568-128">Specifies the site friendly name.</span></span>
<span data-ttu-id="8f568-129">Use esse parâmetro se você estiver baixando as credenciais do cofre para um site do Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="8f568-129">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

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

### <span data-ttu-id="8f568-130">-SiteIdentifier</span><span class="sxs-lookup"><span data-stu-id="8f568-130">-SiteIdentifier</span></span>
<span data-ttu-id="8f568-131">Especifica o identificador do site.</span><span class="sxs-lookup"><span data-stu-id="8f568-131">Specifies the site identifier.</span></span>
<span data-ttu-id="8f568-132">Use esse parâmetro se você estiver baixando as credenciais do cofre para um site do Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="8f568-132">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

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

### <span data-ttu-id="8f568-133">-SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="8f568-133">-SiteRecovery</span></span>
<span data-ttu-id="8f568-134">Indica que o arquivo de credenciais do cofre se aplica ao Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="8f568-134">Indicates the vault credentials file is applicable to Azure Site Recovery.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForSite, ByDefault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f568-135">-Cofre</span><span class="sxs-lookup"><span data-stu-id="8f568-135">-Vault</span></span>
<span data-ttu-id="8f568-136">Especifica o objeto do cofre do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="8f568-136">Specifies the Azure Site Recovery vault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8f568-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f568-137">CommonParameters</span></span>
<span data-ttu-id="8f568-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f568-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f568-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f568-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f568-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8f568-140">INPUTS</span></span>

### <span data-ttu-id="8f568-141">Microsoft. Azure. Commands. Recoveryservices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="8f568-141">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>
<span data-ttu-id="8f568-142">Parâmetros: cofre (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8f568-142">Parameters: Vault (ByValue)</span></span>

## <span data-ttu-id="8f568-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8f568-143">OUTPUTS</span></span>

### <span data-ttu-id="8f568-144">Microsoft. Azure. Commands. Recoveryservices. VaultSettingsFilePath</span><span class="sxs-lookup"><span data-stu-id="8f568-144">Microsoft.Azure.Commands.RecoveryServices.VaultSettingsFilePath</span></span>

## <span data-ttu-id="8f568-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8f568-145">NOTES</span></span>

## <span data-ttu-id="8f568-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8f568-146">RELATED LINKS</span></span>

[<span data-ttu-id="8f568-147">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="8f568-147">Get-AzureRmRecoveryServicesVault</span></span>](./Get-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="8f568-148">New-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="8f568-148">New-AzureRmRecoveryServicesVault</span></span>](./New-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="8f568-149">Remove-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="8f568-149">Remove-AzureRmRecoveryServicesVault</span></span>](./Remove-AzureRmRecoveryServicesVault.md)


