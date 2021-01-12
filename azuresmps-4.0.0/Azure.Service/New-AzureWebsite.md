---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: FBB55071-454D-4473-93BA-D97F33067785
online version: ''
schema: 2.0.0
ms.openlocfilehash: 768eff2dda32c6dfa0bad14f028338d3c5fa1abd
ms.sourcegitcommit: 87730c7ea4f98f628d3fe1b40aa4a9d2885e1c75
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/12/2021
ms.locfileid: "98110471"
---
# <span data-ttu-id="042b6-101">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="042b6-101">New-AzureWebsite</span></span>

## <span data-ttu-id="042b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="042b6-102">SYNOPSIS</span></span>
<span data-ttu-id="042b6-103">Crie um novo site para ser executado no Azure.</span><span class="sxs-lookup"><span data-stu-id="042b6-103">Create a new website to run in Azure.</span></span>

## <span data-ttu-id="042b6-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="042b6-104">SYNTAX</span></span>

```
New-AzureWebsite [-Location <String>] [-Hostname <String>] [-PublishingUsername <String>] [-Git] [-GitHub]
 [-GitHubCredentials <PSCredential>] [-GitHubRepository <String>] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="042b6-105">DESCRIÇÃO</span><span class="sxs-lookup"><span data-stu-id="042b6-105">DESCRIPTION</span></span>
<span data-ttu-id="042b6-106">Este tópico descreve o cmdlet na versão 0.8.10 do módulo Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="042b6-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="042b6-107">Para obter a versão do módulo que você está usando, no console do Azure PowerShell, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="042b6-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="042b6-108">O cmdlet cria um novo site para ser executado no Azure e se prepara para implantação por meio do GitHub.</span><span class="sxs-lookup"><span data-stu-id="042b6-108">The cmdlet creates a new website to run in Azure and prepares for deployment through GitHub.</span></span>

## <span data-ttu-id="042b6-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="042b6-109">EXAMPLES</span></span>

### <span data-ttu-id="042b6-110">Exemplo 1: Criar um novo site com o Git</span><span class="sxs-lookup"><span data-stu-id="042b6-110">Example 1: Create a new website with Git</span></span>
```
PS C:\> New-AzureWebsite mySite -Git
```

<span data-ttu-id="042b6-111">Este exemplo cria um novo site no Azure e um repositório git local a ser usado para implantar arquivos no novo site.</span><span class="sxs-lookup"><span data-stu-id="042b6-111">This example creates a new website in Azure and a local Git repository to use for deploying files to the new website.</span></span>

### <span data-ttu-id="042b6-112">Exemplo 2: Criar site integrado ao GitHub</span><span class="sxs-lookup"><span data-stu-id="042b6-112">Example 2: Create website integrated with GitHub</span></span>
```
PS C:\> New-AzureWebsite mysite -GitHub -GitHubRepository myaccount/myrepo
```

<span data-ttu-id="042b6-113">Este exemplo cria um novo site vinculado a um repositório do GitHub chamado myaccount/myrepo.</span><span class="sxs-lookup"><span data-stu-id="042b6-113">This example creates a new website linked to a GitHub repository named myaccount/myrepo.</span></span>
<span data-ttu-id="042b6-114">As confirmações no repositório do GitHub são adiadas para o site no Azure.</span><span class="sxs-lookup"><span data-stu-id="042b6-114">Commits to the GitHub repository are pushed to the website in Azure.</span></span>

## <span data-ttu-id="042b6-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="042b6-115">PARAMETERS</span></span>

### <span data-ttu-id="042b6-116">-Git</span><span class="sxs-lookup"><span data-stu-id="042b6-116">-Git</span></span>
<span data-ttu-id="042b6-117">Configura um repositório local do Git e o vincula ao site.</span><span class="sxs-lookup"><span data-stu-id="042b6-117">Sets up a local Git repository and links it to the website.</span></span>
<span data-ttu-id="042b6-118">Se especificado, este parâmetro configura um repositório git no diretório local e adiciona um repositório remoto chamado 'azure' que se vincula ao site no Azure.</span><span class="sxs-lookup"><span data-stu-id="042b6-118">If specified, this parameter sets up a Git repository in the local directory and add a remote repository named 'azure' that links to the website in Azure.</span></span>

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

### <span data-ttu-id="042b6-119">-GitHub</span><span class="sxs-lookup"><span data-stu-id="042b6-119">-GitHub</span></span>
<span data-ttu-id="042b6-120">Indica que esse cmdlet vincula o novo site a um repositório existente do GitHub.</span><span class="sxs-lookup"><span data-stu-id="042b6-120">Indicates that this cmdlet links the new website to an existing GitHub repository.</span></span>
<span data-ttu-id="042b6-121">Confirmações para o repositório Giuthub são pressionadas para o site no Azure.</span><span class="sxs-lookup"><span data-stu-id="042b6-121">Commits to the Giuthub repository are pushed to the website in Azure.</span></span>

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

### <span data-ttu-id="042b6-122">-GitHubCredentials</span><span class="sxs-lookup"><span data-stu-id="042b6-122">-GitHubCredentials</span></span>
<span data-ttu-id="042b6-123">Especifica as credenciais de nome de usuário e senha para se conectar ao GitHub.</span><span class="sxs-lookup"><span data-stu-id="042b6-123">Specifies the user name and password credentials to connect to GitHub.</span></span>

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

### <span data-ttu-id="042b6-124">-GitHubRepository</span><span class="sxs-lookup"><span data-stu-id="042b6-124">-GitHubRepository</span></span>
<span data-ttu-id="042b6-125">Especifica o nome completo do repositório do GitHub para vincular a este site.</span><span class="sxs-lookup"><span data-stu-id="042b6-125">Specifies the full name of the GitHub repository to link to this website.</span></span>
<span data-ttu-id="042b6-126">Por exemplo, `myaccount/myrepo` .</span><span class="sxs-lookup"><span data-stu-id="042b6-126">For example, `myaccount/myrepo`.</span></span>

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

### <span data-ttu-id="042b6-127">-Hostname</span><span class="sxs-lookup"><span data-stu-id="042b6-127">-Hostname</span></span>
<span data-ttu-id="042b6-128">Especifica um nome de host alternativo para o novo site.</span><span class="sxs-lookup"><span data-stu-id="042b6-128">Specifies an alternative host name for the new website.</span></span>

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

### <span data-ttu-id="042b6-129">-Location</span><span class="sxs-lookup"><span data-stu-id="042b6-129">-Location</span></span>
<span data-ttu-id="042b6-130">Especifica o local do data center onde você deseja implantar o site.</span><span class="sxs-lookup"><span data-stu-id="042b6-130">Specifies the location of the data center where you want to deploy the website.</span></span>

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

### <span data-ttu-id="042b6-131">-Name</span><span class="sxs-lookup"><span data-stu-id="042b6-131">-Name</span></span>
<span data-ttu-id="042b6-132">Especifica um nome para o site.</span><span class="sxs-lookup"><span data-stu-id="042b6-132">Specifies a name for the website.</span></span>

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

### <span data-ttu-id="042b6-133">-Profile</span><span class="sxs-lookup"><span data-stu-id="042b6-133">-Profile</span></span>
<span data-ttu-id="042b6-134">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="042b6-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="042b6-135">Se você não especificar um perfil, este cmdlet lê do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="042b6-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="042b6-136">-PublishingUsername</span><span class="sxs-lookup"><span data-stu-id="042b6-136">-PublishingUsername</span></span>
<span data-ttu-id="042b6-137">Especifica o nome de usuário especificado na implantação do Portal do Azure para Git.</span><span class="sxs-lookup"><span data-stu-id="042b6-137">Specifies the user name you have specified in the Azure Portal for Git deployment.</span></span>

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

### <span data-ttu-id="042b6-138">-Slot</span><span class="sxs-lookup"><span data-stu-id="042b6-138">-Slot</span></span>
<span data-ttu-id="042b6-139">Especifica um nome de slot para o site.</span><span class="sxs-lookup"><span data-stu-id="042b6-139">Specifies a slot name for the website.</span></span>

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

### <span data-ttu-id="042b6-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="042b6-140">CommonParameters</span></span>
<span data-ttu-id="042b6-141">Este cmdlet oferece suporte aos parâmetros comuns: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="042b6-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="042b6-142">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="042b6-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="042b6-143">ENTRADAS</span><span class="sxs-lookup"><span data-stu-id="042b6-143">INPUTS</span></span>

## <span data-ttu-id="042b6-144">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="042b6-144">OUTPUTS</span></span>

## <span data-ttu-id="042b6-145">OBSERVAÇÕES</span><span class="sxs-lookup"><span data-stu-id="042b6-145">NOTES</span></span>

## <span data-ttu-id="042b6-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="042b6-146">RELATED LINKS</span></span>

[<span data-ttu-id="042b6-147">Set-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="042b6-147">Set-AzureWebsite</span></span>](./Set-AzureWebsite.md)


