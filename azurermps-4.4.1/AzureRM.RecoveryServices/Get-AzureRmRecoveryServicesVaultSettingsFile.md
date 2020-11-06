---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 56074606-28A6-4F91-A56C-4C8A9A31543F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVaultSettingsFile.md
ms.openlocfilehash: 603cd65195f9e33c5006dcb4f2dc98ffc64aa7a3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433027"
---
# <span data-ttu-id="b9505-101">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="b9505-101">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>

## <span data-ttu-id="b9505-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b9505-102">SYNOPSIS</span></span>
<span data-ttu-id="b9505-103">Obtém o arquivo de configurações do cofre do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="b9505-103">Gets the Azure Site Recovery vault settings file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9505-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b9505-104">SYNTAX</span></span>

### <span data-ttu-id="b9505-105">ForSite</span><span class="sxs-lookup"><span data-stu-id="b9505-105">ForSite</span></span>
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> -SiteIdentifier <String>
 -SiteFriendlyName <String> [[-Path] <String>] [-SiteRecovery] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b9505-106">ByDefault</span><span class="sxs-lookup"><span data-stu-id="b9505-106">ByDefault</span></span>
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] [-SiteRecovery]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b9505-107">ForBackupVaultType</span><span class="sxs-lookup"><span data-stu-id="b9505-107">ForBackupVaultType</span></span>
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] [-Backup]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9505-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b9505-108">DESCRIPTION</span></span>
<span data-ttu-id="b9505-109">O cmdlet **Get-AzureRmRecoveryServicesVaultSettingsFile** Obtém o arquivo de configurações para um cofre do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="b9505-109">The **Get-AzureRmRecoveryServicesVaultSettingsFile** cmdlet gets the settings file for an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="b9505-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b9505-110">EXAMPLES</span></span>

### <span data-ttu-id="b9505-111">Exemplo 1: registrar um servidor Windows ou um computador do DPM para backup do Azure</span><span class="sxs-lookup"><span data-stu-id="b9505-111">Example 1: Register a Windows Server or DPM machine for Azure Backup</span></span>
```
PS C:\> $Vault01 = Get-AzureRmRecoveryServicesVault -Name "TestVault"
PS C:\> $CredsPath = "C:\Downloads"
PS C:\> $Credsfilename = Get-AzureRmRecoveryServicesVaultSettingsFile -Backup -Vault $Vault01 -Path $CredsPath
```

<span data-ttu-id="b9505-112">O primeiro comando obtém o cofre chamado TestVault e, em seguida, armazena-o na variável $Vault 01.</span><span class="sxs-lookup"><span data-stu-id="b9505-112">The first command gets the vault named TestVault, and then stores it in the $Vault01 variable.</span></span>

<span data-ttu-id="b9505-113">O segundo comando define a variável $CredsPath como C:\Downloads.</span><span class="sxs-lookup"><span data-stu-id="b9505-113">The second command sets the $CredsPath variable to C:\Downloads.</span></span>

<span data-ttu-id="b9505-114">O último comando obtém o arquivo de credenciais do cofre para $Vault 01 usando as credenciais do $CredsPath para o backup do Azure.</span><span class="sxs-lookup"><span data-stu-id="b9505-114">The last command gets the vault credentials file for $Vault01 using the credentials in $CredsPath for Azure Backup.</span></span>

## <span data-ttu-id="b9505-115">OS</span><span class="sxs-lookup"><span data-stu-id="b9505-115">PARAMETERS</span></span>

### <span data-ttu-id="b9505-116">-Backup</span><span class="sxs-lookup"><span data-stu-id="b9505-116">-Backup</span></span>
<span data-ttu-id="b9505-117">Indica que o arquivo de credenciais do cofre se aplica ao Azure backup.</span><span class="sxs-lookup"><span data-stu-id="b9505-117">Indicates the vault credentials file is applicable to Azure Backup.</span></span>

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

### <span data-ttu-id="b9505-118">-Caminho</span><span class="sxs-lookup"><span data-stu-id="b9505-118">-Path</span></span>
<span data-ttu-id="b9505-119">Especifica o caminho para o arquivo de configurações do cofre do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="b9505-119">Specifies the path to the Azure Site Recovery vault settings file.</span></span>
<span data-ttu-id="b9505-120">Você pode baixar esse arquivo do portal de cofre do Azure site Recovery e armazená-lo localmente.</span><span class="sxs-lookup"><span data-stu-id="b9505-120">You can download this file from the Azure Site Recovery vault portal and store it locally.</span></span>

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

### <span data-ttu-id="b9505-121">-SiteFriendlyName</span><span class="sxs-lookup"><span data-stu-id="b9505-121">-SiteFriendlyName</span></span>
<span data-ttu-id="b9505-122">Especifica o nome amigável do site.</span><span class="sxs-lookup"><span data-stu-id="b9505-122">Specifies the site friendly name.</span></span>
<span data-ttu-id="b9505-123">Use esse parâmetro se você estiver baixando as credenciais do cofre para um site do Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="b9505-123">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

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

### <span data-ttu-id="b9505-124">-SiteIdentifier</span><span class="sxs-lookup"><span data-stu-id="b9505-124">-SiteIdentifier</span></span>
<span data-ttu-id="b9505-125">Especifica o identificador do site.</span><span class="sxs-lookup"><span data-stu-id="b9505-125">Specifies the site identifier.</span></span>
<span data-ttu-id="b9505-126">Use esse parâmetro se você estiver baixando as credenciais do cofre para um site do Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="b9505-126">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

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

### <span data-ttu-id="b9505-127">-SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="b9505-127">-SiteRecovery</span></span>
<span data-ttu-id="b9505-128">Indica que o arquivo de credenciais do cofre se aplica ao Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="b9505-128">Indicates the vault credentials file is applicable to Azure Site Recovery.</span></span>

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

### <span data-ttu-id="b9505-129">-Cofre</span><span class="sxs-lookup"><span data-stu-id="b9505-129">-Vault</span></span>
<span data-ttu-id="b9505-130">Especifica o objeto do cofre do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="b9505-130">Specifies the Azure Site Recovery vault object.</span></span>

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

### <span data-ttu-id="b9505-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9505-131">-DefaultProfile</span></span>
<span data-ttu-id="b9505-132">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b9505-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9505-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9505-133">CommonParameters</span></span>
<span data-ttu-id="b9505-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9505-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9505-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9505-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9505-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b9505-136">INPUTS</span></span>

### <span data-ttu-id="b9505-137">ARSVault</span><span class="sxs-lookup"><span data-stu-id="b9505-137">ARSVault</span></span>
<span data-ttu-id="b9505-138">O parâmetro ' cofre ' aceita o valor do tipo ' ARSVault ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="b9505-138">Parameter 'Vault' accepts value of type 'ARSVault' from the pipeline</span></span>

## <span data-ttu-id="b9505-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b9505-139">OUTPUTS</span></span>

### <span data-ttu-id="b9505-140">Microsoft. Azure. Commands. Recoveryservices. VaultSettingsFilePath</span><span class="sxs-lookup"><span data-stu-id="b9505-140">Microsoft.Azure.Commands.RecoveryServices.VaultSettingsFilePath</span></span>

## <span data-ttu-id="b9505-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b9505-141">NOTES</span></span>

## <span data-ttu-id="b9505-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b9505-142">RELATED LINKS</span></span>

[<span data-ttu-id="b9505-143">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="b9505-143">Get-AzureRmRecoveryServicesVault</span></span>](./Get-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="b9505-144">New-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="b9505-144">New-AzureRmRecoveryServicesVault</span></span>](./New-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="b9505-145">Remove-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="b9505-145">Remove-AzureRmRecoveryServicesVault</span></span>](./Remove-AzureRmRecoveryServicesVault.md)


