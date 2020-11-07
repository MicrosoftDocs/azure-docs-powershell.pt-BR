---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 56074606-28A6-4F91-A56C-4C8A9A31543F
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultSettingsFile.md
ms.openlocfilehash: ac293211c332d8e99a592eedf96bbc179be99912
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944713"
---
# <span data-ttu-id="25b1b-101">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="25b1b-101">Get-AzRecoveryServicesVaultSettingsFile</span></span>

## <span data-ttu-id="25b1b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="25b1b-102">SYNOPSIS</span></span>
<span data-ttu-id="25b1b-103">Obtém o arquivo de configurações do cofre do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="25b1b-103">Gets the Azure Site Recovery vault settings file.</span></span>

## <span data-ttu-id="25b1b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="25b1b-104">SYNTAX</span></span>

### <span data-ttu-id="25b1b-105">ForSiteWithCertificate</span><span class="sxs-lookup"><span data-stu-id="25b1b-105">ForSiteWithCertificate</span></span>
```
Get-AzRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] -SiteIdentifier <String>
 -Certificate <String> -SiteFriendlyName <String> [-SiteRecovery] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="25b1b-106">ByDefaultWithCertificate</span><span class="sxs-lookup"><span data-stu-id="25b1b-106">ByDefaultWithCertificate</span></span>
```
Get-AzRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] -Certificate <String>
 [-SiteRecovery] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25b1b-107">ForBackupVaultTypeWithCertificate</span><span class="sxs-lookup"><span data-stu-id="25b1b-107">ForBackupVaultTypeWithCertificate</span></span>
```
Get-AzRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] -Certificate <String> [-Backup]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25b1b-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="25b1b-108">DESCRIPTION</span></span>
<span data-ttu-id="25b1b-109">O cmdlet **Get-AzRecoveryServicesVaultSettingsFile** Obtém o arquivo de configurações para um cofre do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="25b1b-109">The **Get-AzRecoveryServicesVaultSettingsFile** cmdlet gets the settings file for an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="25b1b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="25b1b-110">EXAMPLES</span></span>

### <span data-ttu-id="25b1b-111">Exemplo 1: registrar um servidor Windows ou um computador do DPM para backup do Azure</span><span class="sxs-lookup"><span data-stu-id="25b1b-111">Example 1: Register a Windows Server or DPM machine for Azure Backup</span></span>
```
PS C:\> $Vault01 = Get-AzRecoveryServicesVault -Name "TestVault"
PS C:\> $CredsPath = "C:\Downloads"
PS C:\> $Credsfilename = Get-AzRecoveryServicesVaultSettingsFile -Backup -Vault $Vault01 -Path $CredsPath
```

<span data-ttu-id="25b1b-112">O primeiro comando obtém o cofre chamado TestVault e, em seguida, armazena-o na variável $Vault 01.</span><span class="sxs-lookup"><span data-stu-id="25b1b-112">The first command gets the vault named TestVault, and then stores it in the $Vault01 variable.</span></span>
<span data-ttu-id="25b1b-113">O segundo comando define a variável $CredsPath como C:\Downloads.</span><span class="sxs-lookup"><span data-stu-id="25b1b-113">The second command sets the $CredsPath variable to C:\Downloads.</span></span>
<span data-ttu-id="25b1b-114">O último comando obtém o arquivo de credenciais do cofre para $Vault 01 usando as credenciais do $CredsPath para o backup do Azure.</span><span class="sxs-lookup"><span data-stu-id="25b1b-114">The last command gets the vault credentials file for $Vault01 using the credentials in $CredsPath for Azure Backup.</span></span>

### <span data-ttu-id="25b1b-115">Exemplo 2:</span><span class="sxs-lookup"><span data-stu-id="25b1b-115">Example 2:</span></span>
```
PS C:\> $Credsfilename = Get-AzRecoveryServicesVaultSettingsFile -SiteIdentifier -Vault $Vault01
```

<span data-ttu-id="25b1b-116">O comando obtém o arquivo de credenciais do cofre para $Vault 01 do cofre do tipo de siteRecovery.</span><span class="sxs-lookup"><span data-stu-id="25b1b-116">The command gets the vault credentials file for $Vault01 of vault type siteRecovery.</span></span>

### <span data-ttu-id="25b1b-117">Exemplo 3: registrar um servidor Windows ou uma máquina do DPM para backup do Azure</span><span class="sxs-lookup"><span data-stu-id="25b1b-117">Example 3: Register a Windows Server or DPM machine for Azure Backup</span></span>
```
PS C:\> $Credsfilename = Get-AzRecoveryServicesVaultSettingsFile -SiteIdentifier -Vault $Vault01
```

<span data-ttu-id="25b1b-118">O comando obtém o arquivo de credenciais do cofre para $Vault 01.</span><span class="sxs-lookup"><span data-stu-id="25b1b-118">The command gets the vault credentials file for $Vault01.</span></span>

## <span data-ttu-id="25b1b-119">OS</span><span class="sxs-lookup"><span data-stu-id="25b1b-119">PARAMETERS</span></span>

### <span data-ttu-id="25b1b-120">-Backup</span><span class="sxs-lookup"><span data-stu-id="25b1b-120">-Backup</span></span>
<span data-ttu-id="25b1b-121">Indica que o arquivo de credenciais do cofre se aplica ao Azure backup.</span><span class="sxs-lookup"><span data-stu-id="25b1b-121">Indicates the vault credentials file is applicable to Azure Backup.</span></span>

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

### <span data-ttu-id="25b1b-122">-Certificado</span><span class="sxs-lookup"><span data-stu-id="25b1b-122">-Certificate</span></span>
<span data-ttu-id="25b1b-123">{{Fill descrição do certificado}}</span><span class="sxs-lookup"><span data-stu-id="25b1b-123">{{Fill Certificate Description}}</span></span>

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

### <span data-ttu-id="25b1b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25b1b-124">-DefaultProfile</span></span>
<span data-ttu-id="25b1b-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="25b1b-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25b1b-126">-Caminho</span><span class="sxs-lookup"><span data-stu-id="25b1b-126">-Path</span></span>
<span data-ttu-id="25b1b-127">Especifica o caminho para o arquivo de configurações do cofre do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="25b1b-127">Specifies the path to the Azure Site Recovery vault settings file.</span></span>
<span data-ttu-id="25b1b-128">Você pode baixar esse arquivo do portal de cofre do Azure site Recovery e armazená-lo localmente.</span><span class="sxs-lookup"><span data-stu-id="25b1b-128">You can download this file from the Azure Site Recovery vault portal and store it locally.</span></span>

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

### <span data-ttu-id="25b1b-129">-SiteFriendlyName</span><span class="sxs-lookup"><span data-stu-id="25b1b-129">-SiteFriendlyName</span></span>
<span data-ttu-id="25b1b-130">Especifica o nome amigável do site.</span><span class="sxs-lookup"><span data-stu-id="25b1b-130">Specifies the site friendly name.</span></span>
<span data-ttu-id="25b1b-131">Use esse parâmetro se você estiver baixando as credenciais do cofre para um site do Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="25b1b-131">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

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

### <span data-ttu-id="25b1b-132">-SiteIdentifier</span><span class="sxs-lookup"><span data-stu-id="25b1b-132">-SiteIdentifier</span></span>
<span data-ttu-id="25b1b-133">Especifica o identificador do site.</span><span class="sxs-lookup"><span data-stu-id="25b1b-133">Specifies the site identifier.</span></span>
<span data-ttu-id="25b1b-134">Use esse parâmetro se você estiver baixando as credenciais do cofre para um site do Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="25b1b-134">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

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

### <span data-ttu-id="25b1b-135">-SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="25b1b-135">-SiteRecovery</span></span>
<span data-ttu-id="25b1b-136">Indica que o arquivo de credenciais do cofre se aplica ao Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="25b1b-136">Indicates the vault credentials file is applicable to Azure Site Recovery.</span></span>

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

### <span data-ttu-id="25b1b-137">-Cofre</span><span class="sxs-lookup"><span data-stu-id="25b1b-137">-Vault</span></span>
<span data-ttu-id="25b1b-138">Especifica o objeto do cofre do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="25b1b-138">Specifies the Azure Site Recovery vault object.</span></span>

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

### <span data-ttu-id="25b1b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25b1b-139">CommonParameters</span></span>
<span data-ttu-id="25b1b-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25b1b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25b1b-141">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="25b1b-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25b1b-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="25b1b-142">INPUTS</span></span>

### <span data-ttu-id="25b1b-143">Microsoft. Azure. Commands. Recoveryservices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="25b1b-143">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="25b1b-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="25b1b-144">OUTPUTS</span></span>

### <span data-ttu-id="25b1b-145">Microsoft. Azure. Commands. Recoveryservices. VaultSettingsFilePath</span><span class="sxs-lookup"><span data-stu-id="25b1b-145">Microsoft.Azure.Commands.RecoveryServices.VaultSettingsFilePath</span></span>

## <span data-ttu-id="25b1b-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="25b1b-146">NOTES</span></span>

## <span data-ttu-id="25b1b-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="25b1b-147">RELATED LINKS</span></span>

[<span data-ttu-id="25b1b-148">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="25b1b-148">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="25b1b-149">New-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="25b1b-149">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)

[<span data-ttu-id="25b1b-150">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="25b1b-150">Remove-AzRecoveryServicesVault</span></span>](./Remove-AzRecoveryServicesVault.md)


