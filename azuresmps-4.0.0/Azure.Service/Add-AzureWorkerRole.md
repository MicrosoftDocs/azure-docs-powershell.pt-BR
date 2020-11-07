---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 8632A865-D4CC-4AE5-8307-055CDD776D26
online version: ''
schema: 2.0.0
ms.openlocfilehash: a2b79ee50bb5097896c2a120a9b7316adb2146b5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945710"
---
# <span data-ttu-id="369fd-101">Add-AzureWorkerRole</span><span class="sxs-lookup"><span data-stu-id="369fd-101">Add-AzureWorkerRole</span></span>

## <span data-ttu-id="369fd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="369fd-102">SYNOPSIS</span></span>
<span data-ttu-id="369fd-103">Cria arquivos obrigatórios e configuração para uma função de trabalhador personalizada.</span><span class="sxs-lookup"><span data-stu-id="369fd-103">Creates required files and configuration for a custom worker role.</span></span>

## <span data-ttu-id="369fd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="369fd-104">SYNTAX</span></span>

```
Add-AzureWorkerRole [-TemplateFolder <String>] [-Name <String>] [-Instances <Int32>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="369fd-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="369fd-105">DESCRIPTION</span></span>
<span data-ttu-id="369fd-106">Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="369fd-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="369fd-107">Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="369fd-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="369fd-108">O cmdlet **Add-AzureWorkerRole** cria arquivos e configurações necessários, às vezes chamados de scaffolding, para uma função de trabalhador personalizada.</span><span class="sxs-lookup"><span data-stu-id="369fd-108">The **Add-AzureWorkerRole** cmdlet creates required files and configuration, sometimes referred to as scaffolding, for a custom worker role.</span></span>

## <span data-ttu-id="369fd-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="369fd-109">EXAMPLES</span></span>

### <span data-ttu-id="369fd-110">Exemplo 1: criar uma única função de trabalho de instância</span><span class="sxs-lookup"><span data-stu-id="369fd-110">Example 1: Create a single instance worker role</span></span>
```
PS C:\> Add-AzureWorkerRole -Name MyWorkerRole
```

<span data-ttu-id="369fd-111">Este exemplo adiciona scaffolding para uma única função de trabalho chamada MyWorkerRole ao aplicativo atual.</span><span class="sxs-lookup"><span data-stu-id="369fd-111">This example adds scaffolding for a single worker role named MyWorkerRole to the current application.</span></span>

### <span data-ttu-id="369fd-112">Exemplo 2: criar uma função de trabalho de várias instâncias</span><span class="sxs-lookup"><span data-stu-id="369fd-112">Example 2: Create a multiple instance worker role</span></span>
```
PS C:\> Add-AzureWorkerRole MyWorkerRole -I 2
```

<span data-ttu-id="369fd-113">Este exemplo adiciona scaffolding para uma nova função de trabalho chamada MyWorkerRole ao aplicativo atual, com uma contagem de instância de função 2.</span><span class="sxs-lookup"><span data-stu-id="369fd-113">This example adds scaffolding for a new worker role named MyWorkerRole to the current application, with a role instance count of 2.</span></span>

### <span data-ttu-id="369fd-114">Exemplo 3: criar função de trabalho com o scaffolding personalizado</span><span class="sxs-lookup"><span data-stu-id="369fd-114">Example 3: Create worker role with custom scaffolding</span></span>
```
PS C:\> Add-AzureWorkerRole MyWorkerRole -TemplateFoldr .\MyWorkerRoleTemplate
```

<span data-ttu-id="369fd-115">Este exemplo cria uma função de trabalho com scaffolding personalizado.</span><span class="sxs-lookup"><span data-stu-id="369fd-115">This example creates a worker role with custom scaffolding.</span></span>

## <span data-ttu-id="369fd-116">OS</span><span class="sxs-lookup"><span data-stu-id="369fd-116">PARAMETERS</span></span>

### <span data-ttu-id="369fd-117">-Instâncias</span><span class="sxs-lookup"><span data-stu-id="369fd-117">-Instances</span></span>
<span data-ttu-id="369fd-118">Especifica o número de instâncias de função para esta função de trabalho.</span><span class="sxs-lookup"><span data-stu-id="369fd-118">Specifies the number of role instances for this worker role.</span></span>
<span data-ttu-id="369fd-119">O padrão é 1.</span><span class="sxs-lookup"><span data-stu-id="369fd-119">The default is 1.</span></span>

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

### <span data-ttu-id="369fd-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="369fd-120">-Name</span></span>
<span data-ttu-id="369fd-121">Especifica o nome da função de trabalho.</span><span class="sxs-lookup"><span data-stu-id="369fd-121">Specifies the name of the worker role.</span></span>
<span data-ttu-id="369fd-122">Esse valor determina o nome da pasta que contém o scaffolding para o aplicativo personalizado que será hospedado na função de trabalho.</span><span class="sxs-lookup"><span data-stu-id="369fd-122">This value determines the folder name that contains the scaffolding for the custom application that will be hosted in the worker role.</span></span>
<span data-ttu-id="369fd-123">O padrão é WorkerRolenumber, em que núm é o número de funções de trabalho no serviço.</span><span class="sxs-lookup"><span data-stu-id="369fd-123">The default is WorkerRolenumber, where number is the number of worker roles in the service.</span></span>

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

### <span data-ttu-id="369fd-124">-Perfil</span><span class="sxs-lookup"><span data-stu-id="369fd-124">-Profile</span></span>
<span data-ttu-id="369fd-125">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="369fd-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="369fd-126">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="369fd-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="369fd-127">-TemplateFolder</span><span class="sxs-lookup"><span data-stu-id="369fd-127">-TemplateFolder</span></span>
<span data-ttu-id="369fd-128">Especifica a pasta de modelos do scaffolding a ser usada para criar a função de trabalho.</span><span class="sxs-lookup"><span data-stu-id="369fd-128">Specifies the scaffolding template folder to be used to create the worker role.</span></span>

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

### <span data-ttu-id="369fd-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="369fd-129">CommonParameters</span></span>
<span data-ttu-id="369fd-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="369fd-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="369fd-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="369fd-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="369fd-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="369fd-132">INPUTS</span></span>

## <span data-ttu-id="369fd-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="369fd-133">OUTPUTS</span></span>

## <span data-ttu-id="369fd-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="369fd-134">NOTES</span></span>

## <span data-ttu-id="369fd-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="369fd-135">RELATED LINKS</span></span>

[<span data-ttu-id="369fd-136">Add-AzureWebRole</span><span class="sxs-lookup"><span data-stu-id="369fd-136">Add-AzureWebRole</span></span>](./Add-AzureWebRole.md)

[<span data-ttu-id="369fd-137">New-AzureRoleTemplate</span><span class="sxs-lookup"><span data-stu-id="369fd-137">New-AzureRoleTemplate</span></span>](./New-AzureRoleTemplate.md)


