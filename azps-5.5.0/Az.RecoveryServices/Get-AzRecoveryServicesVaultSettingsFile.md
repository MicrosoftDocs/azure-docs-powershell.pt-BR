---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 56074606-28A6-4F91-A56C-4C8A9A31543F
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultSettingsFile.md
ms.openlocfilehash: 0d074c18ad9b5f9ea34a465acd4a91a88d4b69ac
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114947"
---
# <span data-ttu-id="c6fbf-101">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="c6fbf-101">Get-AzRecoveryServicesVaultSettingsFile</span></span>

## <span data-ttu-id="c6fbf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c6fbf-102">SYNOPSIS</span></span>
<span data-ttu-id="c6fbf-103">Obtém o arquivo de configurações do cofre de Recuperação de Site do Azure.</span><span class="sxs-lookup"><span data-stu-id="c6fbf-103">Gets the Azure Site Recovery vault settings file.</span></span>

## <span data-ttu-id="c6fbf-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c6fbf-104">SYNTAX</span></span>

### <span data-ttu-id="c6fbf-105">ForSiteWithCertificate</span><span class="sxs-lookup"><span data-stu-id="c6fbf-105">ForSiteWithCertificate</span></span>
```
Get-AzRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] -SiteIdentifier <String>
 -Certificate <String> -SiteFriendlyName <String> [-SiteRecovery] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c6fbf-106">ByDefaultWithCertificate</span><span class="sxs-lookup"><span data-stu-id="c6fbf-106">ByDefaultWithCertificate</span></span>
```
Get-AzRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] -Certificate <String>
 [-SiteRecovery] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c6fbf-107">ForBackupVaultTypeWithCertificate</span><span class="sxs-lookup"><span data-stu-id="c6fbf-107">ForBackupVaultTypeWithCertificate</span></span>
```
Get-AzRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] -Certificate <String> [-Backup]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c6fbf-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="c6fbf-108">DESCRIPTION</span></span>
<span data-ttu-id="c6fbf-109">O cmdlet **Get-AzRecoveryServicesVaultSettingsFile** obtém o arquivo de configurações de um cofre de Recuperação de Site do Azure.</span><span class="sxs-lookup"><span data-stu-id="c6fbf-109">The **Get-AzRecoveryServicesVaultSettingsFile** cmdlet gets the settings file for an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="c6fbf-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c6fbf-110">EXAMPLES</span></span>

### <span data-ttu-id="c6fbf-111">Exemplo 1: Registrar um computador Windows Server ou DPM para Backup do Azure</span><span class="sxs-lookup"><span data-stu-id="c6fbf-111">Example 1: Register a Windows Server or DPM machine for Azure Backup</span></span>
```powershell
PS C:\> $Vault01 = Get-AzRecoveryServicesVault -Name "TestVault"
PS C:\> $CredsPath = "C:\Downloads"
PS C:\> $Credsfilename = Get-AzRecoveryServicesVaultSettingsFile -Backup -Vault $Vault01 -Path $CredsPath
```

<span data-ttu-id="c6fbf-112">O primeiro comando obtém o cofre chamado TestVault e o armazena na variável $Vault 01.</span><span class="sxs-lookup"><span data-stu-id="c6fbf-112">The first command gets the vault named TestVault, and then stores it in the $Vault01 variable.</span></span>
<span data-ttu-id="c6fbf-113">O segundo comando define a $CredsPath variável como C:\Downloads.</span><span class="sxs-lookup"><span data-stu-id="c6fbf-113">The second command sets the $CredsPath variable to C:\Downloads.</span></span>
<span data-ttu-id="c6fbf-114">O último comando obtém o arquivo de credenciais do cofre para $Vault 01 usando as credenciais no $CredsPath backup do Azure.</span><span class="sxs-lookup"><span data-stu-id="c6fbf-114">The last command gets the vault credentials file for $Vault01 using the credentials in $CredsPath for Azure Backup.</span></span>

### <span data-ttu-id="c6fbf-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="c6fbf-115">Example 2</span></span>
```powershell
PS C:\> $Credsfilename = Get-AzRecoveryServicesVaultSettingsFile -SiteIdentifier -Vault $Vault01
```

<span data-ttu-id="c6fbf-116">O comando obtém o arquivo de credenciais do cofre $Vault 01 de Recuperação do site de tipo de cofre.</span><span class="sxs-lookup"><span data-stu-id="c6fbf-116">The command gets the vault credentials file for $Vault01 of vault type siteRecovery.</span></span>

### <span data-ttu-id="c6fbf-117">Exemplo 3: Registrar um computador Windows Server ou DPM para Backup do Azure</span><span class="sxs-lookup"><span data-stu-id="c6fbf-117">Example 3: Register a Windows Server or DPM machine for Azure Backup</span></span>
```powershell
PS C:\> $Credsfilename = Get-AzRecoveryServicesVaultSettingsFile -SiteIdentifier -Vault $Vault01
```

<span data-ttu-id="c6fbf-118">O comando obtém o arquivo de credenciais do cofre para $Vault 01.</span><span class="sxs-lookup"><span data-stu-id="c6fbf-118">The command gets the vault credentials file for $Vault01.</span></span>

## <span data-ttu-id="c6fbf-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c6fbf-119">PARAMETERS</span></span>

### <span data-ttu-id="c6fbf-120">-Backup</span><span class="sxs-lookup"><span data-stu-id="c6fbf-120">-Backup</span></span>
<span data-ttu-id="c6fbf-121">Indica que o arquivo de credenciais do cofre é aplicável ao Backup do Azure.</span><span class="sxs-lookup"><span data-stu-id="c6fbf-121">Indicates the vault credentials file is applicable to Azure Backup.</span></span>

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

### <span data-ttu-id="c6fbf-122">-Certificado</span><span class="sxs-lookup"><span data-stu-id="c6fbf-122">-Certificate</span></span>
<span data-ttu-id="c6fbf-123">{{Fill Certificate Description}}</span><span class="sxs-lookup"><span data-stu-id="c6fbf-123">{{Fill Certificate Description}}</span></span>

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

### <span data-ttu-id="c6fbf-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6fbf-124">-DefaultProfile</span></span>
<span data-ttu-id="c6fbf-125">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="c6fbf-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6fbf-126">-Caminho</span><span class="sxs-lookup"><span data-stu-id="c6fbf-126">-Path</span></span>
<span data-ttu-id="c6fbf-127">Especifica o caminho para o arquivo de configurações do cofre de Recuperação de Site do Azure.</span><span class="sxs-lookup"><span data-stu-id="c6fbf-127">Specifies the path to the Azure Site Recovery vault settings file.</span></span>
<span data-ttu-id="c6fbf-128">Você pode baixar esse arquivo do portal do cofre de Recuperação de Site do Azure e armazená-lo localmente.</span><span class="sxs-lookup"><span data-stu-id="c6fbf-128">You can download this file from the Azure Site Recovery vault portal and store it locally.</span></span>

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

### <span data-ttu-id="c6fbf-129">-SiteName</span><span class="sxs-lookup"><span data-stu-id="c6fbf-129">-SiteFriendlyName</span></span>
<span data-ttu-id="c6fbf-130">Especifica o nome amigável do site.</span><span class="sxs-lookup"><span data-stu-id="c6fbf-130">Specifies the site friendly name.</span></span>
<span data-ttu-id="c6fbf-131">Use este parâmetro se você estiver baixando as credenciais do cofre para um site Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="c6fbf-131">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

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

### <span data-ttu-id="c6fbf-132">-SiteIdentifier</span><span class="sxs-lookup"><span data-stu-id="c6fbf-132">-SiteIdentifier</span></span>
<span data-ttu-id="c6fbf-133">Especifica o identificador do site.</span><span class="sxs-lookup"><span data-stu-id="c6fbf-133">Specifies the site identifier.</span></span>
<span data-ttu-id="c6fbf-134">Use este parâmetro se você estiver baixando as credenciais do cofre para um site Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="c6fbf-134">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

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

### <span data-ttu-id="c6fbf-135">-SiteRecuprecupação</span><span class="sxs-lookup"><span data-stu-id="c6fbf-135">-SiteRecovery</span></span>
<span data-ttu-id="c6fbf-136">Indica que o arquivo de credenciais do cofre é aplicável à Recuperação de Site do Azure.</span><span class="sxs-lookup"><span data-stu-id="c6fbf-136">Indicates the vault credentials file is applicable to Azure Site Recovery.</span></span>

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

### <span data-ttu-id="c6fbf-137">-Cofre</span><span class="sxs-lookup"><span data-stu-id="c6fbf-137">-Vault</span></span>
<span data-ttu-id="c6fbf-138">Especifica o objeto do cofre de Recuperação de Site do Azure.</span><span class="sxs-lookup"><span data-stu-id="c6fbf-138">Specifies the Azure Site Recovery vault object.</span></span>

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

### <span data-ttu-id="c6fbf-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6fbf-139">CommonParameters</span></span>
<span data-ttu-id="c6fbf-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6fbf-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6fbf-141">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c6fbf-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6fbf-142">Entradas</span><span class="sxs-lookup"><span data-stu-id="c6fbf-142">INPUTS</span></span>

### <span data-ttu-id="c6fbf-143">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="c6fbf-143">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="c6fbf-144">Saídas</span><span class="sxs-lookup"><span data-stu-id="c6fbf-144">OUTPUTS</span></span>

### <span data-ttu-id="c6fbf-145">Microsoft.Azure.Commands.RecoveryServices.VaultSettingsFilePath</span><span class="sxs-lookup"><span data-stu-id="c6fbf-145">Microsoft.Azure.Commands.RecoveryServices.VaultSettingsFilePath</span></span>

## <span data-ttu-id="c6fbf-146">Notas</span><span class="sxs-lookup"><span data-stu-id="c6fbf-146">NOTES</span></span>

## <span data-ttu-id="c6fbf-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c6fbf-147">RELATED LINKS</span></span>

[<span data-ttu-id="c6fbf-148">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="c6fbf-148">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="c6fbf-149">New-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="c6fbf-149">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)

[<span data-ttu-id="c6fbf-150">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="c6fbf-150">Remove-AzRecoveryServicesVault</span></span>](./Remove-AzRecoveryServicesVault.md)


