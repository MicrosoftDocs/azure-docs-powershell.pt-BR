---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: F9A06B8B-55DB-48A5-B246-53347E759E64
online version: ''
schema: 2.0.0
ms.openlocfilehash: 050c05f2cdad546388744bcebca4f28a12a03038
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946390"
---
# <span data-ttu-id="cc360-101">Add-AzurePHPWebRole</span><span class="sxs-lookup"><span data-stu-id="cc360-101">Add-AzurePHPWebRole</span></span>

## <span data-ttu-id="cc360-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cc360-102">SYNOPSIS</span></span>
<span data-ttu-id="cc360-103">Cria os arquivos necessários e a configuração para um aplicativo PHP.</span><span class="sxs-lookup"><span data-stu-id="cc360-103">Creates the required files and configuration for a PHP application.</span></span>

## <span data-ttu-id="cc360-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cc360-104">SYNTAX</span></span>

```
Add-AzurePHPWebRole [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="cc360-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cc360-105">DESCRIPTION</span></span>
<span data-ttu-id="cc360-106">Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="cc360-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="cc360-107">Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="cc360-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="cc360-108">O cmdlet **Add-AzurePHPWebRole** cria os arquivos e a configuração, às vezes chamados de scaffolding, para um aplicativo PHP que será hospedado no Azure pelo IIS.</span><span class="sxs-lookup"><span data-stu-id="cc360-108">The **Add-AzurePHPWebRole** cmdlet creates the files and configuration, sometimes referred to as scaffolding, for a PHP application that will be hosted in Azure through IIS.</span></span>

## <span data-ttu-id="cc360-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cc360-109">EXAMPLES</span></span>

### <span data-ttu-id="cc360-110">Exemplo 1: adicionar uma função da Web usando valores padrão</span><span class="sxs-lookup"><span data-stu-id="cc360-110">Example 1: Add a web role using default values</span></span>
```
PS C:\> Add-AzurePHPWebRole
```

<span data-ttu-id="cc360-111">Este exemplo adiciona os arquivos e a configuração necessários para a nova função da Web usando os valores padrão de um serviço chamado "WebRole1" com 1 instância.</span><span class="sxs-lookup"><span data-stu-id="cc360-111">This example adds the required files and configuration for new web role using the default values of a service named "WebRole1" with 1 instance.</span></span>

### <span data-ttu-id="cc360-112">Exemplo 2: adicionar uma função da Web com várias instâncias</span><span class="sxs-lookup"><span data-stu-id="cc360-112">Example 2: Add a web role with multiple instances</span></span>
```
PS C:\> Add-AzurePHPWebRole MyWebRole -I 2
```

<span data-ttu-id="cc360-113">Este exemplo adiciona os arquivos e a configuração necessários para uma nova função da Web ao aplicativo atual, usando o nome "MyWebRole" e uma contagem de instâncias de função 2.</span><span class="sxs-lookup"><span data-stu-id="cc360-113">This example adds the required files and configuration for a new web role to the current application, using the name "MyWebRole" and a role instance count of 2.</span></span>

## <span data-ttu-id="cc360-114">OS</span><span class="sxs-lookup"><span data-stu-id="cc360-114">PARAMETERS</span></span>

### <span data-ttu-id="cc360-115">-Instâncias</span><span class="sxs-lookup"><span data-stu-id="cc360-115">-Instances</span></span>
<span data-ttu-id="cc360-116">Especifica o número de instâncias de função para esta função da Web.</span><span class="sxs-lookup"><span data-stu-id="cc360-116">Specifies the number of role instances for this web role.</span></span>
<span data-ttu-id="cc360-117">O padrão é 1.</span><span class="sxs-lookup"><span data-stu-id="cc360-117">The default is 1.</span></span>

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

### <span data-ttu-id="cc360-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="cc360-118">-Name</span></span>
<span data-ttu-id="cc360-119">Especifica o nome da função da Web.</span><span class="sxs-lookup"><span data-stu-id="cc360-119">Specifies the name of the web role.</span></span>
<span data-ttu-id="cc360-120">O nome determina o nome do diretório que contém os arquivos necessários e a configuração para o aplicativo PHP.</span><span class="sxs-lookup"><span data-stu-id="cc360-120">The name determines the name of the directory that contains the required files and configuration for the PHP application.</span></span>
<span data-ttu-id="cc360-121">O padrão é WebRole #, em que # é o número de funções da Web no serviço.</span><span class="sxs-lookup"><span data-stu-id="cc360-121">The default is WebRole#, where # is the number of web roles in the service.</span></span>

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

### <span data-ttu-id="cc360-122">-Perfil</span><span class="sxs-lookup"><span data-stu-id="cc360-122">-Profile</span></span>
<span data-ttu-id="cc360-123">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="cc360-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="cc360-124">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="cc360-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="cc360-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc360-125">CommonParameters</span></span>
<span data-ttu-id="cc360-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc360-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc360-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc360-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc360-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cc360-128">INPUTS</span></span>

## <span data-ttu-id="cc360-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cc360-129">OUTPUTS</span></span>

## <span data-ttu-id="cc360-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cc360-130">NOTES</span></span>

## <span data-ttu-id="cc360-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cc360-131">RELATED LINKS</span></span>

[<span data-ttu-id="cc360-132">Add-AzurePHPWorkerRole</span><span class="sxs-lookup"><span data-stu-id="cc360-132">Add-AzurePHPWorkerRole</span></span>](./Add-AzurePHPWorkerRole.md)

[<span data-ttu-id="cc360-133">New-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="cc360-133">New-AzureServiceProject</span></span>](./New-AzureServiceProject.md)


