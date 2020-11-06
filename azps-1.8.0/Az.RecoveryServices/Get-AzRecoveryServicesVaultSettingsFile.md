---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 56074606-28A6-4F91-A56C-4C8A9A31543F
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultSettingsFile.md
ms.openlocfilehash: 5455babba58e050397066e5439b3e046315b4101
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599680"
---
# <span data-ttu-id="ad566-101">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="ad566-101">Get-AzRecoveryServicesVaultSettingsFile</span></span>

## <span data-ttu-id="ad566-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ad566-102">SYNOPSIS</span></span>
<span data-ttu-id="ad566-103">Obtém o arquivo de configurações do cofre do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="ad566-103">Gets the Azure Site Recovery vault settings file.</span></span>

## <span data-ttu-id="ad566-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ad566-104">SYNTAX</span></span>

### <span data-ttu-id="ad566-105">ForSiteWithCertificate</span><span class="sxs-lookup"><span data-stu-id="ad566-105">ForSiteWithCertificate</span></span>
```
Get-AzRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] -SiteIdentifier <String>
 -Certificate <String> -SiteFriendlyName <String> [-SiteRecovery] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ad566-106">ByDefaultWithCertificate</span><span class="sxs-lookup"><span data-stu-id="ad566-106">ByDefaultWithCertificate</span></span>
```
Get-AzRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] -Certificate <String>
 [-SiteRecovery] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ad566-107">ForBackupVaultTypeWithCertificate</span><span class="sxs-lookup"><span data-stu-id="ad566-107">ForBackupVaultTypeWithCertificate</span></span>
```
Get-AzRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] -Certificate <String> [-Backup]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad566-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ad566-108">DESCRIPTION</span></span>
<span data-ttu-id="ad566-109">O cmdlet **Get-AzRecoveryServicesVaultSettingsFile** Obtém o arquivo de configurações para um cofre do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="ad566-109">The **Get-AzRecoveryServicesVaultSettingsFile** cmdlet gets the settings file for an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="ad566-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ad566-110">EXAMPLES</span></span>

### <span data-ttu-id="ad566-111">Exemplo 1: registrar um servidor Windows ou um computador do DPM para backup do Azure</span><span class="sxs-lookup"><span data-stu-id="ad566-111">Example 1: Register a Windows Server or DPM machine for Azure Backup</span></span>
```
PS C:\> $Vault01 = Get-AzRecoveryServicesVault -Name "TestVault"
PS C:\> $CredsPath = "C:\Downloads"
PS C:\> $Credsfilename = Get-AzRecoveryServicesVaultSettingsFile -Backup -Vault $Vault01 -Path $CredsPath
```

<span data-ttu-id="ad566-112">O primeiro comando obtém o cofre chamado TestVault e, em seguida, armazena-o na variável $Vault 01.</span><span class="sxs-lookup"><span data-stu-id="ad566-112">The first command gets the vault named TestVault, and then stores it in the $Vault01 variable.</span></span>
<span data-ttu-id="ad566-113">O segundo comando define a variável $CredsPath como C:\Downloads.</span><span class="sxs-lookup"><span data-stu-id="ad566-113">The second command sets the $CredsPath variable to C:\Downloads.</span></span>
<span data-ttu-id="ad566-114">O último comando obtém o arquivo de credenciais do cofre para $Vault 01 usando as credenciais do $CredsPath para o backup do Azure.</span><span class="sxs-lookup"><span data-stu-id="ad566-114">The last command gets the vault credentials file for $Vault01 using the credentials in $CredsPath for Azure Backup.</span></span>

### <span data-ttu-id="ad566-115">Exemplo 2:</span><span class="sxs-lookup"><span data-stu-id="ad566-115">Example 2:</span></span>
```
PS C:\> $Credsfilename = Get-AzRecoveryServicesVaultSettingsFile -SiteIdentifier -Vault $Vault01
```

<span data-ttu-id="ad566-116">O comando obtém o arquivo de credenciais do cofre para $Vault 01 do cofre do tipo de siteRecovery.</span><span class="sxs-lookup"><span data-stu-id="ad566-116">The command gets the vault credentials file for $Vault01 of vault type siteRecovery.</span></span>

### <span data-ttu-id="ad566-117">Exemplo 3: registrar um servidor Windows ou uma máquina do DPM para backup do Azure</span><span class="sxs-lookup"><span data-stu-id="ad566-117">Example 3: Register a Windows Server or DPM machine for Azure Backup</span></span>
```
PS C:\> $Credsfilename = Get-AzRecoveryServicesVaultSettingsFile -SiteIdentifier -Vault $Vault01
```

<span data-ttu-id="ad566-118">O comando obtém o arquivo de credenciais do cofre para $Vault 01.</span><span class="sxs-lookup"><span data-stu-id="ad566-118">The command gets the vault credentials file for $Vault01.</span></span>

## <span data-ttu-id="ad566-119">OS</span><span class="sxs-lookup"><span data-stu-id="ad566-119">PARAMETERS</span></span>

### <span data-ttu-id="ad566-120">-Backup</span><span class="sxs-lookup"><span data-stu-id="ad566-120">-Backup</span></span>
<span data-ttu-id="ad566-121">Indica que o arquivo de credenciais do cofre se aplica ao Azure backup.</span><span class="sxs-lookup"><span data-stu-id="ad566-121">Indicates the vault credentials file is applicable to Azure Backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForBackupVaultTypeWithCertificate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad566-122">-Certificado</span><span class="sxs-lookup"><span data-stu-id="ad566-122">-Certificate</span></span>
<span data-ttu-id="ad566-123">{{Fill descrição do certificado}}</span><span class="sxs-lookup"><span data-stu-id="ad566-123">{{Fill Certificate Description}}</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad566-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad566-124">-DefaultProfile</span></span>
<span data-ttu-id="ad566-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ad566-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad566-126">-Caminho</span><span class="sxs-lookup"><span data-stu-id="ad566-126">-Path</span></span>
<span data-ttu-id="ad566-127">Especifica o caminho para o arquivo de configurações do cofre do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="ad566-127">Specifies the path to the Azure Site Recovery vault settings file.</span></span>
<span data-ttu-id="ad566-128">Você pode baixar esse arquivo do portal de cofre do Azure site Recovery e armazená-lo localmente.</span><span class="sxs-lookup"><span data-stu-id="ad566-128">You can download this file from the Azure Site Recovery vault portal and store it locally.</span></span>

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

### <span data-ttu-id="ad566-129">-SiteFriendlyName</span><span class="sxs-lookup"><span data-stu-id="ad566-129">-SiteFriendlyName</span></span>
<span data-ttu-id="ad566-130">Especifica o nome amigável do site.</span><span class="sxs-lookup"><span data-stu-id="ad566-130">Specifies the site friendly name.</span></span>
<span data-ttu-id="ad566-131">Use esse parâmetro se você estiver baixando as credenciais do cofre para um site do Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="ad566-131">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

```yaml
Type: System.String
Parameter Sets: ForSiteWithCertificate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad566-132">-SiteIdentifier</span><span class="sxs-lookup"><span data-stu-id="ad566-132">-SiteIdentifier</span></span>
<span data-ttu-id="ad566-133">Especifica o identificador do site.</span><span class="sxs-lookup"><span data-stu-id="ad566-133">Specifies the site identifier.</span></span>
<span data-ttu-id="ad566-134">Use esse parâmetro se você estiver baixando as credenciais do cofre para um site do Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="ad566-134">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

```yaml
Type: System.String
Parameter Sets: ForSiteWithCertificate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad566-135">-SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="ad566-135">-SiteRecovery</span></span>
<span data-ttu-id="ad566-136">Indica que o arquivo de credenciais do cofre se aplica ao Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="ad566-136">Indicates the vault credentials file is applicable to Azure Site Recovery.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForSiteWithCertificate, ByDefaultWithCertificate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad566-137">-Cofre</span><span class="sxs-lookup"><span data-stu-id="ad566-137">-Vault</span></span>
<span data-ttu-id="ad566-138">Especifica o objeto do cofre do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="ad566-138">Specifies the Azure Site Recovery vault object.</span></span>

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

### <span data-ttu-id="ad566-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad566-139">CommonParameters</span></span>
<span data-ttu-id="ad566-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad566-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad566-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad566-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad566-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ad566-142">INPUTS</span></span>

### <span data-ttu-id="ad566-143">Microsoft. Azure. Commands. Recoveryservices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="ad566-143">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="ad566-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ad566-144">OUTPUTS</span></span>

### <span data-ttu-id="ad566-145">Microsoft. Azure. Commands. Recoveryservices. VaultSettingsFilePath</span><span class="sxs-lookup"><span data-stu-id="ad566-145">Microsoft.Azure.Commands.RecoveryServices.VaultSettingsFilePath</span></span>

## <span data-ttu-id="ad566-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ad566-146">NOTES</span></span>

## <span data-ttu-id="ad566-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ad566-147">RELATED LINKS</span></span>

[<span data-ttu-id="ad566-148">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="ad566-148">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="ad566-149">New-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="ad566-149">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)

[<span data-ttu-id="ad566-150">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="ad566-150">Remove-AzRecoveryServicesVault</span></span>](./Remove-AzRecoveryServicesVault.md)


