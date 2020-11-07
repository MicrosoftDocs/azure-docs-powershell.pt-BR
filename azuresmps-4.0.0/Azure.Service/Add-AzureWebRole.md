---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: FB5CD696-108D-4A3E-8983-1C6562E8795A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 25ade8ccf395d37ab0856742fe473a6508c9d63b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945711"
---
# <span data-ttu-id="f3364-101">Add-AzureWebRole</span><span class="sxs-lookup"><span data-stu-id="f3364-101">Add-AzureWebRole</span></span>

## <span data-ttu-id="f3364-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f3364-102">SYNOPSIS</span></span>
<span data-ttu-id="f3364-103">Adiciona uma função de trabalho da Web.</span><span class="sxs-lookup"><span data-stu-id="f3364-103">Adds a web worker role.</span></span>

## <span data-ttu-id="f3364-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f3364-104">SYNTAX</span></span>

```
Add-AzureWebRole [-TemplateFolder <String>] [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="f3364-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f3364-105">DESCRIPTION</span></span>
<span data-ttu-id="f3364-106">Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f3364-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="f3364-107">Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="f3364-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="f3364-108">O cmdlet **Add-AzureWebRole** adiciona uma função de trabalho da Web.</span><span class="sxs-lookup"><span data-stu-id="f3364-108">The **Add-AzureWebRole** cmdlet adds a web worker role.</span></span>

## <span data-ttu-id="f3364-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f3364-109">EXAMPLES</span></span>

### <span data-ttu-id="f3364-110">Exemplo 1: adicionar uma função padrão</span><span class="sxs-lookup"><span data-stu-id="f3364-110">Example 1: Add a default role</span></span>
```
PS C:\> Add-AzureWebRole
```

<span data-ttu-id="f3364-111">Esse comando adiciona a função da Web que tem a configuração padrão de Webrole1 como o nome e uma única instância.</span><span class="sxs-lookup"><span data-stu-id="f3364-111">This command add web role that has the default configuration of Webrole1 as the name and a single instance.</span></span>

### <span data-ttu-id="f3364-112">Exemplo 2: adicionar uma função com um nome</span><span class="sxs-lookup"><span data-stu-id="f3364-112">Example 2: Add a role with a name</span></span>
```
PS C:\> Add-AzureWebRole -Name "MyWebRole"
```

<span data-ttu-id="f3364-113">Esse comando adiciona uma única função da Web chamada MyWebRole ao aplicativo atual.</span><span class="sxs-lookup"><span data-stu-id="f3364-113">This command adds a single web role named MyWebRole to the current application.</span></span>

### <span data-ttu-id="f3364-114">Exemplo 3: adicionar uma função com um nome e uma contagem de instâncias</span><span class="sxs-lookup"><span data-stu-id="f3364-114">Example 3: Add a role with a name and instance count</span></span>
```
PS C:\> Add-AzureWebRole -Name "MyWebRole" -Instance 2
```

<span data-ttu-id="f3364-115">Esse comando adiciona uma função da Web chamada MyWebRole ao aplicativo atual.</span><span class="sxs-lookup"><span data-stu-id="f3364-115">This command adds a web role named MyWebRole to the current application.</span></span>
<span data-ttu-id="f3364-116">O cmdlet tem uma contagem de instâncias de função 2.</span><span class="sxs-lookup"><span data-stu-id="f3364-116">The cmdlet has a role instance count of 2.</span></span>

### <span data-ttu-id="f3364-117">Exemplo 4: adicionar uma função com um nome e um modelo</span><span class="sxs-lookup"><span data-stu-id="f3364-117">Example 4: Add a role with a name and template</span></span>
```
PS C:\> Add-AzureWebRole -Name "MyWebRole" -TemplateFolder ".\MyWebTemplateFolder"
```

<span data-ttu-id="f3364-118">Esse comando adiciona uma única função da Web chamada MyWebRole ao aplicativo atual.</span><span class="sxs-lookup"><span data-stu-id="f3364-118">This command adds a single web role named MyWebRole to the current application.</span></span>
<span data-ttu-id="f3364-119">O comando especifica uma pasta chamada MyWebTemplateFolder como um modelo scaffolding.</span><span class="sxs-lookup"><span data-stu-id="f3364-119">The command specifies a folder named MyWebTemplateFolder as a scaffolding template.</span></span>

## <span data-ttu-id="f3364-120">OS</span><span class="sxs-lookup"><span data-stu-id="f3364-120">PARAMETERS</span></span>

### <span data-ttu-id="f3364-121">-Instâncias</span><span class="sxs-lookup"><span data-stu-id="f3364-121">-Instances</span></span>
<span data-ttu-id="f3364-122">Especifica o número de instâncias.</span><span class="sxs-lookup"><span data-stu-id="f3364-122">Specifies the number of instances.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: i

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3364-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="f3364-123">-Name</span></span>
<span data-ttu-id="f3364-124">Especifica o nome da função da Web.</span><span class="sxs-lookup"><span data-stu-id="f3364-124">Specifies the name of the web role.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: n

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3364-125">-Perfil</span><span class="sxs-lookup"><span data-stu-id="f3364-125">-Profile</span></span>
<span data-ttu-id="f3364-126">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="f3364-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f3364-127">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="f3364-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f3364-128">-TemplateFolder</span><span class="sxs-lookup"><span data-stu-id="f3364-128">-TemplateFolder</span></span>
<span data-ttu-id="f3364-129">Especifica a pasta do modelo.</span><span class="sxs-lookup"><span data-stu-id="f3364-129">Specifies the template folder.</span></span>

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

### <span data-ttu-id="f3364-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3364-130">CommonParameters</span></span>
<span data-ttu-id="f3364-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3364-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3364-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3364-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3364-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f3364-133">INPUTS</span></span>

## <span data-ttu-id="f3364-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f3364-134">OUTPUTS</span></span>

## <span data-ttu-id="f3364-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f3364-135">NOTES</span></span>

## <span data-ttu-id="f3364-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f3364-136">RELATED LINKS</span></span>

[<span data-ttu-id="f3364-137">Add-AzureWorkerRole</span><span class="sxs-lookup"><span data-stu-id="f3364-137">Add-AzureWorkerRole</span></span>](./Add-AzureWorkerRole.md)

[<span data-ttu-id="f3364-138">New-AzureRoleTemplate</span><span class="sxs-lookup"><span data-stu-id="f3364-138">New-AzureRoleTemplate</span></span>](./New-AzureRoleTemplate.md)


