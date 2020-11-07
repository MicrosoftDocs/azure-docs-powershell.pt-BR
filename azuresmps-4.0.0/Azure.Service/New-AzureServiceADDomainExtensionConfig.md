---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: DFD4BA63-A7DE-49DD-878C-68062EF17873
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4d4830d049ab01142c75847b4afd5419729f14d1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945897"
---
# <span data-ttu-id="23442-101">New-AzureServiceADDomainExtensionConfig</span><span class="sxs-lookup"><span data-stu-id="23442-101">New-AzureServiceADDomainExtensionConfig</span></span>

## <span data-ttu-id="23442-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="23442-102">SYNOPSIS</span></span>
<span data-ttu-id="23442-103">Gera a configuração da extensão de domínio do AD para serviços de nuvem.</span><span class="sxs-lookup"><span data-stu-id="23442-103">Generates the configuration for the AD domain extension for cloud services.</span></span>

## <span data-ttu-id="23442-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="23442-104">SYNTAX</span></span>

### <span data-ttu-id="23442-105">JoinDomainUsingEnumOptions (padrão)</span><span class="sxs-lookup"><span data-stu-id="23442-105">JoinDomainUsingEnumOptions (Default)</span></span>
```
New-AzureServiceADDomainExtensionConfig [[-Role] <String[]>] [[-X509Certificate] <X509Certificate2>]
 [[-ThumbprintAlgorithm] <String>] [-DomainName] <String> [-Restart] [[-Credential] <PSCredential>]
 [[-UnjoinDomainCredential] <PSCredential>] [[-Options] <JoinOptions>] [[-OUPath] <String>]
 [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="23442-106">JoinDomainUsingJoinOption</span><span class="sxs-lookup"><span data-stu-id="23442-106">JoinDomainUsingJoinOption</span></span>
```
New-AzureServiceADDomainExtensionConfig [[-Role] <String[]>] [[-X509Certificate] <X509Certificate2>]
 [[-ThumbprintAlgorithm] <String>] [-DomainName] <String> [-Restart] [[-Credential] <PSCredential>]
 [[-UnjoinDomainCredential] <PSCredential>] [-JoinOption] <UInt32> [[-OUPath] <String>] [[-Version] <String>]
 [[-ExtensionId] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="23442-107">WorkGroupName</span><span class="sxs-lookup"><span data-stu-id="23442-107">WorkGroupName</span></span>
```
New-AzureServiceADDomainExtensionConfig [[-Role] <String[]>] [[-X509Certificate] <X509Certificate2>]
 [[-ThumbprintAlgorithm] <String>] [-WorkgroupName] <String> [-Restart] [[-Credential] <PSCredential>]
 [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="23442-108">JoinDomainUsingEnumOptionsAndThumbprint</span><span class="sxs-lookup"><span data-stu-id="23442-108">JoinDomainUsingEnumOptionsAndThumbprint</span></span>
```
New-AzureServiceADDomainExtensionConfig [[-Role] <String[]>] [-CertificateThumbprint] <String>
 [[-ThumbprintAlgorithm] <String>] [-DomainName] <String> [-Restart] [[-Credential] <PSCredential>]
 [[-UnjoinDomainCredential] <PSCredential>] [[-Options] <JoinOptions>] [[-OUPath] <String>]
 [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="23442-109">JoinDomainUsingJoinOptionAndThumbprint</span><span class="sxs-lookup"><span data-stu-id="23442-109">JoinDomainUsingJoinOptionAndThumbprint</span></span>
```
New-AzureServiceADDomainExtensionConfig [[-Role] <String[]>] [-CertificateThumbprint] <String>
 [[-ThumbprintAlgorithm] <String>] [-DomainName] <String> [-Restart] [[-Credential] <PSCredential>]
 [[-UnjoinDomainCredential] <PSCredential>] [-JoinOption] <UInt32> [[-OUPath] <String>] [[-Version] <String>]
 [[-ExtensionId] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="23442-110">WorkGroupNameThumbprint</span><span class="sxs-lookup"><span data-stu-id="23442-110">WorkGroupNameThumbprint</span></span>
```
New-AzureServiceADDomainExtensionConfig [[-Role] <String[]>] [-CertificateThumbprint] <String>
 [[-ThumbprintAlgorithm] <String>] [-WorkgroupName] <String> [-Restart] [[-Credential] <PSCredential>]
 [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="23442-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="23442-111">DESCRIPTION</span></span>
<span data-ttu-id="23442-112">O cmdlet **New-AzureServiceADDomainExtensionConfig** gera a configuração da extensão de domínio do Active Directory (AD) para serviços de nuvem.</span><span class="sxs-lookup"><span data-stu-id="23442-112">The **New-AzureServiceADDomainExtensionConfig** cmdlet generates the configuration for the Active Directory (AD) domain extension for cloud services.</span></span>

## <span data-ttu-id="23442-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="23442-113">EXAMPLES</span></span>

### <span data-ttu-id="23442-114">Exemplo 1: especificar uma configuração de domínio do AD</span><span class="sxs-lookup"><span data-stu-id="23442-114">Example 1: Specify an AD domain configuration</span></span>
```
PS C:\> $ExtensionCfg = New-AzureServiceADDomainExtensionConfig -Role WorkerRole1 -DomainName $Domain -Credential $Cred -JoinOption 35;

PS C:\> New-AzureDeployment -ServiceName $CloudSvc -Slot "Production" -Package $Pkg -Configuration $Config -ExtensionConfiguration $ExtensionCfg;
```

<span data-ttu-id="23442-115">Esse comando gera uma configuração para a extensão de domínio do anúncio.</span><span class="sxs-lookup"><span data-stu-id="23442-115">This command generates a configuration for the AD domain extension.</span></span>

## <span data-ttu-id="23442-116">OS</span><span class="sxs-lookup"><span data-stu-id="23442-116">PARAMETERS</span></span>

### <span data-ttu-id="23442-117">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="23442-117">-CertificateThumbprint</span></span>
<span data-ttu-id="23442-118">Especifica uma impressão digital de certificado a ser usada para criptografar a configuração particular.</span><span class="sxs-lookup"><span data-stu-id="23442-118">Specifies a certificate thumbprint to use to encrypt the private configuration.</span></span>
<span data-ttu-id="23442-119">Este certificado já existe no repositório de certificados.</span><span class="sxs-lookup"><span data-stu-id="23442-119">This certificate has to already exist in the certificate store.</span></span>
<span data-ttu-id="23442-120">Se você não especificar um certificado, esse cmdlet criará um certificado.</span><span class="sxs-lookup"><span data-stu-id="23442-120">If you do not specify a certificate, this cmdlet creates a certificate.</span></span>

```yaml
Type: String
Parameter Sets: JoinDomainUsingEnumOptionsAndThumbprint, JoinDomainUsingJoinOptionAndThumbprint, WorkGroupNameThumbprint
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23442-121">-Credential</span><span class="sxs-lookup"><span data-stu-id="23442-121">-Credential</span></span>
<span data-ttu-id="23442-122">Especifica as credenciais a serem usadas para ingressar no domínio do AD.</span><span class="sxs-lookup"><span data-stu-id="23442-122">Specifies the credentials to use to join the AD domain.</span></span>
<span data-ttu-id="23442-123">As credenciais incluem um nome de usuário e uma senha.</span><span class="sxs-lookup"><span data-stu-id="23442-123">Credentials include a user name and password.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23442-124">-DomainName</span><span class="sxs-lookup"><span data-stu-id="23442-124">-DomainName</span></span>
<span data-ttu-id="23442-125">Especifica o nome de domínio do anúncio.</span><span class="sxs-lookup"><span data-stu-id="23442-125">Specifies the AD domain name.</span></span>

```yaml
Type: String
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingJoinOption, JoinDomainUsingEnumOptionsAndThumbprint, JoinDomainUsingJoinOptionAndThumbprint
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23442-126">-ExtensionId</span><span class="sxs-lookup"><span data-stu-id="23442-126">-ExtensionId</span></span>
<span data-ttu-id="23442-127">Especifica a ID de extensão.</span><span class="sxs-lookup"><span data-stu-id="23442-127">Specifies the extension ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23442-128">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="23442-128">-InformationAction</span></span>
<span data-ttu-id="23442-129">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="23442-129">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="23442-130">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="23442-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="23442-131">Contínuo</span><span class="sxs-lookup"><span data-stu-id="23442-131">Continue</span></span>
- <span data-ttu-id="23442-132">Ignorar</span><span class="sxs-lookup"><span data-stu-id="23442-132">Ignore</span></span>
- <span data-ttu-id="23442-133">Inquire</span><span class="sxs-lookup"><span data-stu-id="23442-133">Inquire</span></span>
- <span data-ttu-id="23442-134">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="23442-134">SilentlyContinue</span></span>
- <span data-ttu-id="23442-135">Finaliza</span><span class="sxs-lookup"><span data-stu-id="23442-135">Stop</span></span>
- <span data-ttu-id="23442-136">Suspensão</span><span class="sxs-lookup"><span data-stu-id="23442-136">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23442-137">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="23442-137">-InformationVariable</span></span>
<span data-ttu-id="23442-138">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="23442-138">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23442-139">-JoinOption</span><span class="sxs-lookup"><span data-stu-id="23442-139">-JoinOption</span></span>
<span data-ttu-id="23442-140">Especifica a enumeração da opção de junção.</span><span class="sxs-lookup"><span data-stu-id="23442-140">Specifies the join option enumeration.</span></span>

```yaml
Type: UInt32
Parameter Sets: JoinDomainUsingJoinOption, JoinDomainUsingJoinOptionAndThumbprint
Aliases: 

Required: True
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23442-141">-Opções</span><span class="sxs-lookup"><span data-stu-id="23442-141">-Options</span></span>
<span data-ttu-id="23442-142">Especifica a opção de junção de inteiro não assinado.</span><span class="sxs-lookup"><span data-stu-id="23442-142">Specifies the unsigned integer join option.</span></span>

```yaml
Type: JoinOptions
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingEnumOptionsAndThumbprint
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23442-143">-OUPath</span><span class="sxs-lookup"><span data-stu-id="23442-143">-OUPath</span></span>
<span data-ttu-id="23442-144">Especifica o caminho da unidade organizacional (UO) para a operação de ingresso no domínio do AD.</span><span class="sxs-lookup"><span data-stu-id="23442-144">Specifies the organization unit (OU) path for AD domain join operation.</span></span>

```yaml
Type: String
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingJoinOption, JoinDomainUsingEnumOptionsAndThumbprint, JoinDomainUsingJoinOptionAndThumbprint
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23442-145">-Perfil</span><span class="sxs-lookup"><span data-stu-id="23442-145">-Profile</span></span>
<span data-ttu-id="23442-146">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="23442-146">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="23442-147">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="23442-147">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="23442-148">-Restart</span><span class="sxs-lookup"><span data-stu-id="23442-148">-Restart</span></span>
<span data-ttu-id="23442-149">Especifica se o computador deve ser reiniciado se a operação de ingresso for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="23442-149">Specifies whether to restart the computer if the join operation succeeds.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23442-150">-Função</span><span class="sxs-lookup"><span data-stu-id="23442-150">-Role</span></span>
<span data-ttu-id="23442-151">Especifica uma matriz opcional de funções para especificar a configuração da área de trabalho remota para a configuração de domínio do anúncio.</span><span class="sxs-lookup"><span data-stu-id="23442-151">Specifies an optional array of roles to specify the remote desktop configuration for the AD domain configuration.</span></span>
<span data-ttu-id="23442-152">Se você não especificar esse parâmetro, a configuração de domínio do AD será aplicada como a configuração padrão para todas as funções.</span><span class="sxs-lookup"><span data-stu-id="23442-152">If you do not specify this parameter, the AD domain configuration is applied as the default configuration for all roles.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23442-153">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="23442-153">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="23442-154">Especifica um algoritmo de hash de impressão digital que é usado com a impressão digital para identificar o certificado.</span><span class="sxs-lookup"><span data-stu-id="23442-154">Specifies a thumbprint hashing algorithm that is used with the thumbprint to identify the certificate.</span></span>
<span data-ttu-id="23442-155">Esse parâmetro é opcional, e o padrão é SHA1.</span><span class="sxs-lookup"><span data-stu-id="23442-155">This parameter is optional and the default is sha1.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23442-156">-UnjoinDomainCredential</span><span class="sxs-lookup"><span data-stu-id="23442-156">-UnjoinDomainCredential</span></span>
<span data-ttu-id="23442-157">Especifica as credenciais (nome de usuário e senha) para sair do domínio do AD.</span><span class="sxs-lookup"><span data-stu-id="23442-157">Specifies the credentials (user name and password) to unjoin the AD domain.</span></span>

```yaml
Type: PSCredential
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingJoinOption, JoinDomainUsingEnumOptionsAndThumbprint, JoinDomainUsingJoinOptionAndThumbprint
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23442-158">-Versão</span><span class="sxs-lookup"><span data-stu-id="23442-158">-Version</span></span>
<span data-ttu-id="23442-159">Especifica a versão de extensão.</span><span class="sxs-lookup"><span data-stu-id="23442-159">Specifies the extension version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23442-160">-WorkgroupName</span><span class="sxs-lookup"><span data-stu-id="23442-160">-WorkgroupName</span></span>
<span data-ttu-id="23442-161">Especifica o nome do grupo de trabalho.</span><span class="sxs-lookup"><span data-stu-id="23442-161">Specifies the workgroup name.</span></span>

```yaml
Type: String
Parameter Sets: WorkGroupName, WorkGroupNameThumbprint
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23442-162">-X509Certificate</span><span class="sxs-lookup"><span data-stu-id="23442-162">-X509Certificate</span></span>
<span data-ttu-id="23442-163">Especifica um certificado X. 509 que é carregado automaticamente para o serviço de nuvem e usado para criptografar a configuração privada de extensão.</span><span class="sxs-lookup"><span data-stu-id="23442-163">Specifies an X.509 certificate that is automatically uploaded to the cloud service and used for encrypting the extension private configuration.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingJoinOption, WorkGroupName
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23442-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23442-164">CommonParameters</span></span>
<span data-ttu-id="23442-165">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23442-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23442-166">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23442-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23442-167">SENSORES</span><span class="sxs-lookup"><span data-stu-id="23442-167">INPUTS</span></span>

## <span data-ttu-id="23442-168">EXIBE</span><span class="sxs-lookup"><span data-stu-id="23442-168">OUTPUTS</span></span>

## <span data-ttu-id="23442-169">INFORMA</span><span class="sxs-lookup"><span data-stu-id="23442-169">NOTES</span></span>

## <span data-ttu-id="23442-170">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="23442-170">RELATED LINKS</span></span>

[<span data-ttu-id="23442-171">Get-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="23442-171">Get-AzureServiceADDomainExtension</span></span>](./Get-AzureServiceADDomainExtension.md)

[<span data-ttu-id="23442-172">Set-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="23442-172">Set-AzureServiceADDomainExtension</span></span>](./Set-AzureServiceADDomainExtension.md)


