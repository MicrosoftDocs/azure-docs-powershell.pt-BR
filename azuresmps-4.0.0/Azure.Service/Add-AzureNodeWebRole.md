---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: C2DAFB2C-A58B-406C-8349-8728771B279E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 59aef29c27d7eb96834d270c2fce48ff3acb9554
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946392"
---
# <span data-ttu-id="7a839-101">Add-AzureNodeWebRole</span><span class="sxs-lookup"><span data-stu-id="7a839-101">Add-AzureNodeWebRole</span></span>

## <span data-ttu-id="7a839-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7a839-102">SYNOPSIS</span></span>
<span data-ttu-id="7a839-103">Cria arquivos e pastas necessários para um aplicativo Node.js.</span><span class="sxs-lookup"><span data-stu-id="7a839-103">Creates required files and folders for a Node.js application.</span></span>

## <span data-ttu-id="7a839-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7a839-104">SYNTAX</span></span>

```
Add-AzureNodeWebRole [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="7a839-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7a839-105">DESCRIPTION</span></span>
<span data-ttu-id="7a839-106">Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="7a839-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="7a839-107">Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="7a839-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="7a839-108">O **Add-AzureNodeWebRole** cria arquivos e pastas necessários, às vezes chamados de scaffolding, para que um aplicativo Node.js seja hospedado na nuvem via IIS.</span><span class="sxs-lookup"><span data-stu-id="7a839-108">The **Add-AzureNodeWebRole** creates required files and folders, sometimes referred to as scaffolding, for a Node.js application to be hosted in the cloud via IIS.</span></span>

## <span data-ttu-id="7a839-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7a839-109">EXAMPLES</span></span>

### <span data-ttu-id="7a839-110">Exemplo 1: função da Web de instância única</span><span class="sxs-lookup"><span data-stu-id="7a839-110">Example 1: Single instance web role</span></span>
```
PS C:\> Add-AzureNodeWebRole -Name MyWebRole
```

<span data-ttu-id="7a839-111">Este exemplo adiciona scaffolding para uma única função da Web chamada **MyWebRole** ao aplicativo atual.</span><span class="sxs-lookup"><span data-stu-id="7a839-111">This example adds scaffolding for a single web role named **MyWebRole** to the current application.</span></span>

### <span data-ttu-id="7a839-112">Exemplo 2: função da Web com várias instâncias</span><span class="sxs-lookup"><span data-stu-id="7a839-112">Example 2: Multiple instance web role</span></span>
```
PS C:\> Add-AzureNodeWebRole MyWebRole -I 2
```

<span data-ttu-id="7a839-113">Este exemplo adiciona scaffolding para uma nova função da Web chamada **MyWebRole** ao aplicativo atual, com uma contagem de instância de função 2.</span><span class="sxs-lookup"><span data-stu-id="7a839-113">This example adds scaffolding for a new web role named **MyWebRole** to the current application, with a role instance count of 2.</span></span>

## <span data-ttu-id="7a839-114">OS</span><span class="sxs-lookup"><span data-stu-id="7a839-114">PARAMETERS</span></span>

### <span data-ttu-id="7a839-115">-Instâncias</span><span class="sxs-lookup"><span data-stu-id="7a839-115">-Instances</span></span>
<span data-ttu-id="7a839-116">Especifica o número de instâncias de função para esta função da Web.</span><span class="sxs-lookup"><span data-stu-id="7a839-116">Specifies the number of role instances for this web role.</span></span>
<span data-ttu-id="7a839-117">O padrão é 1.</span><span class="sxs-lookup"><span data-stu-id="7a839-117">The default is 1.</span></span>

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

### <span data-ttu-id="7a839-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="7a839-118">-Name</span></span>
<span data-ttu-id="7a839-119">Especifica o nome da função da Web.</span><span class="sxs-lookup"><span data-stu-id="7a839-119">Specifies the name of the web role.</span></span>
<span data-ttu-id="7a839-120">Ele também determina o nome do diretório que contém o scaffolding para o aplicativo node.js que será hospedado na função da Web.</span><span class="sxs-lookup"><span data-stu-id="7a839-120">It also determines the name of the directory that contains the scaffolding for the node.js application that will be hosted in the web role.</span></span>
<span data-ttu-id="7a839-121">O padrão é WebRole #, em que # indica o número de funções da Web no serviço.</span><span class="sxs-lookup"><span data-stu-id="7a839-121">The default is WebRole#, where # indicates the number of web roles in the service.</span></span>

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

### <span data-ttu-id="7a839-122">-Perfil</span><span class="sxs-lookup"><span data-stu-id="7a839-122">-Profile</span></span>
<span data-ttu-id="7a839-123">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="7a839-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7a839-124">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="7a839-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7a839-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a839-125">CommonParameters</span></span>
<span data-ttu-id="7a839-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a839-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a839-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a839-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a839-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7a839-128">INPUTS</span></span>

## <span data-ttu-id="7a839-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7a839-129">OUTPUTS</span></span>

## <span data-ttu-id="7a839-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7a839-130">NOTES</span></span>

## <span data-ttu-id="7a839-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7a839-131">RELATED LINKS</span></span>

[<span data-ttu-id="7a839-132">Add-AzureNodeWorkerRole</span><span class="sxs-lookup"><span data-stu-id="7a839-132">Add-AzureNodeWorkerRole</span></span>](./Add-AzureNodeWorkerRole.md)

[<span data-ttu-id="7a839-133">New-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="7a839-133">New-AzureServiceProject</span></span>](./New-AzureServiceProject.md)


