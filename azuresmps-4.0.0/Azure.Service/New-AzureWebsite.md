---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: FBB55071-454D-4473-93BA-D97F33067785
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0f83489d21fba97bb50145de1fedc1ac9a7195a1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946184"
---
# <span data-ttu-id="7a4b1-101">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="7a4b1-101">New-AzureWebsite</span></span>

## <span data-ttu-id="7a4b1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7a4b1-102">SYNOPSIS</span></span>
<span data-ttu-id="7a4b1-103">Crie um novo site para ser executado no Azure.</span><span class="sxs-lookup"><span data-stu-id="7a4b1-103">Create a new website to run in Azure.</span></span>

## <span data-ttu-id="7a4b1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7a4b1-104">SYNTAX</span></span>

```
New-AzureWebsite [-Location <String>] [-Hostname <String>] [-PublishingUsername <String>] [-Git] [-GitHub]
 [-GithubCredentials <PSCredential>] [-GithubRepository <String>] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="7a4b1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7a4b1-105">DESCRIPTION</span></span>
<span data-ttu-id="7a4b1-106">Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="7a4b1-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="7a4b1-107">Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="7a4b1-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="7a4b1-108">O cmdlet cria um novo site para ser executado no Azure e se prepara para a implantação pelo github.</span><span class="sxs-lookup"><span data-stu-id="7a4b1-108">The cmdlet creates a new website to run in Azure and prepares for deployment through Github.</span></span>

## <span data-ttu-id="7a4b1-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7a4b1-109">EXAMPLES</span></span>

### <span data-ttu-id="7a4b1-110">Exemplo 1: criar um novo site com git</span><span class="sxs-lookup"><span data-stu-id="7a4b1-110">Example 1: Create a new website with Git</span></span>
```
PS C:\> New-AzureWebsite mySite -Git
```

<span data-ttu-id="7a4b1-111">Este exemplo cria um novo site no Azure e um repositório local do git para usar para implantar arquivos no novo site.</span><span class="sxs-lookup"><span data-stu-id="7a4b1-111">This example creates a new website in Azure and a local Git repository to use for deploying files to the new website.</span></span>

### <span data-ttu-id="7a4b1-112">Exemplo 2: criar um site integrado ao github</span><span class="sxs-lookup"><span data-stu-id="7a4b1-112">Example 2: Create website integrated with Github</span></span>
```
PS C:\> New-AzureWebsite mysite -Github -GithubRepository myaccount/myrepo
```

<span data-ttu-id="7a4b1-113">Este exemplo cria um novo site vinculado a um repositório GitHub nomeado myaccount/myrepositório.</span><span class="sxs-lookup"><span data-stu-id="7a4b1-113">This example creates a new website linked to a Github repository named myaccount/myrepo.</span></span>
<span data-ttu-id="7a4b1-114">As confirmações no repositório do GitHub são enviadas para o site do Azure.</span><span class="sxs-lookup"><span data-stu-id="7a4b1-114">Commits to the Github repository are pushed to the website in Azure.</span></span>

## <span data-ttu-id="7a4b1-115">OS</span><span class="sxs-lookup"><span data-stu-id="7a4b1-115">PARAMETERS</span></span>

### <span data-ttu-id="7a4b1-116">-Git</span><span class="sxs-lookup"><span data-stu-id="7a4b1-116">-Git</span></span>
<span data-ttu-id="7a4b1-117">Configura um repositório local do git e o vincula ao site.</span><span class="sxs-lookup"><span data-stu-id="7a4b1-117">Sets up a local Git repository and links it to the website.</span></span>
<span data-ttu-id="7a4b1-118">Se especificado, esse parâmetro configurará um repositório git no diretório local e adicionará um repositório remoto denominado ' Azure ' vinculado ao site do Azure.</span><span class="sxs-lookup"><span data-stu-id="7a4b1-118">If specified, this parameter sets up a Git repository in the local directory and add a remote repository named 'azure' that links to the website in Azure.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a4b1-119">-GitHub</span><span class="sxs-lookup"><span data-stu-id="7a4b1-119">-GitHub</span></span>
<span data-ttu-id="7a4b1-120">Indica que esse cmdlet vincula o novo site a um repositório GitHub existente.</span><span class="sxs-lookup"><span data-stu-id="7a4b1-120">Indicates that this cmdlet links the new website to an existing Github repository.</span></span>
<span data-ttu-id="7a4b1-121">As confirmações no repositório do Giuthub são enviadas para o site do Azure.</span><span class="sxs-lookup"><span data-stu-id="7a4b1-121">Commits to the Giuthub repository are pushed to the website in Azure.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a4b1-122">-GithubCredentials</span><span class="sxs-lookup"><span data-stu-id="7a4b1-122">-GithubCredentials</span></span>
<span data-ttu-id="7a4b1-123">Especifica as credenciais de nome de usuário e senha para se conectar ao github.</span><span class="sxs-lookup"><span data-stu-id="7a4b1-123">Specifies the user name and password credentials to connect to Github.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a4b1-124">-GithubRepository</span><span class="sxs-lookup"><span data-stu-id="7a4b1-124">-GithubRepository</span></span>
<span data-ttu-id="7a4b1-125">Especifica o nome completo do repositório do GitHub para vincular a este site.</span><span class="sxs-lookup"><span data-stu-id="7a4b1-125">Specifies the full name of the Github repository to link to this website.</span></span>
<span data-ttu-id="7a4b1-126">Por exemplo, `myaccount/myrepo` .</span><span class="sxs-lookup"><span data-stu-id="7a4b1-126">For example, `myaccount/myrepo`.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a4b1-127">-Hostname</span><span class="sxs-lookup"><span data-stu-id="7a4b1-127">-Hostname</span></span>
<span data-ttu-id="7a4b1-128">Especifica um nome de host alternativo para o novo site.</span><span class="sxs-lookup"><span data-stu-id="7a4b1-128">Specifies an alternative host name for the new website.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a4b1-129">-Local</span><span class="sxs-lookup"><span data-stu-id="7a4b1-129">-Location</span></span>
<span data-ttu-id="7a4b1-130">Especifica o local do centro de dados onde você deseja implantar o site.</span><span class="sxs-lookup"><span data-stu-id="7a4b1-130">Specifies the location of the data center where you want to deploy the website.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a4b1-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="7a4b1-131">-Name</span></span>
<span data-ttu-id="7a4b1-132">Especifica um nome para o site.</span><span class="sxs-lookup"><span data-stu-id="7a4b1-132">Specifies a name for the website.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a4b1-133">-Perfil</span><span class="sxs-lookup"><span data-stu-id="7a4b1-133">-Profile</span></span>
<span data-ttu-id="7a4b1-134">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="7a4b1-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7a4b1-135">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="7a4b1-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7a4b1-136">-PublishingUsername</span><span class="sxs-lookup"><span data-stu-id="7a4b1-136">-PublishingUsername</span></span>
<span data-ttu-id="7a4b1-137">Especifica o nome de usuário que você especificou no portal do Azure para implantação do git.</span><span class="sxs-lookup"><span data-stu-id="7a4b1-137">Specifies the user name you have specified in the Azure Portal for Git deployment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a4b1-138">-Slot</span><span class="sxs-lookup"><span data-stu-id="7a4b1-138">-Slot</span></span>
<span data-ttu-id="7a4b1-139">Especifica o nome de um slot para o site.</span><span class="sxs-lookup"><span data-stu-id="7a4b1-139">Specifies a slot name for the website.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a4b1-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a4b1-140">CommonParameters</span></span>
<span data-ttu-id="7a4b1-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a4b1-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a4b1-142">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a4b1-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a4b1-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7a4b1-143">INPUTS</span></span>

## <span data-ttu-id="7a4b1-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7a4b1-144">OUTPUTS</span></span>

## <span data-ttu-id="7a4b1-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7a4b1-145">NOTES</span></span>

## <span data-ttu-id="7a4b1-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7a4b1-146">RELATED LINKS</span></span>

[<span data-ttu-id="7a4b1-147">Set-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="7a4b1-147">Set-AzureWebsite</span></span>](./Set-AzureWebsite.md)


