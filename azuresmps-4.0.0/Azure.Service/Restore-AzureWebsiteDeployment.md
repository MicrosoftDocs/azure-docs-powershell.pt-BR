---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: B83ABF05-3169-4D05-AB6E-167DE045595D
online version: ''
schema: 2.0.0
ms.openlocfilehash: fea9341b288b5c2f98413cc95cb42bffe1a78ca3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945463"
---
# <span data-ttu-id="d951f-101">Restore-AzureWebsiteDeployment</span><span class="sxs-lookup"><span data-stu-id="d951f-101">Restore-AzureWebsiteDeployment</span></span>

## <span data-ttu-id="d951f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d951f-102">SYNOPSIS</span></span>
<span data-ttu-id="d951f-103">Reimplanta uma implantação anterior de um site no Azure.</span><span class="sxs-lookup"><span data-stu-id="d951f-103">Redeploys a previous deployment of a website in Azure.</span></span>

## <span data-ttu-id="d951f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d951f-104">SYNTAX</span></span>

```
Restore-AzureWebsiteDeployment [-CommitId <String>] [-Force] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d951f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d951f-105">DESCRIPTION</span></span>
<span data-ttu-id="d951f-106">Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d951f-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="d951f-107">Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="d951f-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="d951f-108">O cmdlet **Restore-AzureWebsiteDeployment** reimplanta uma implantação anterior de um site no Azure.</span><span class="sxs-lookup"><span data-stu-id="d951f-108">The **Restore-AzureWebsiteDeployment** cmdlet redeploys a previous deployment of a website in Azure.</span></span>
<span data-ttu-id="d951f-109">Esse processo substitui a implantação atual pela implantação selecionada.</span><span class="sxs-lookup"><span data-stu-id="d951f-109">This process replaces the current deployment with the selected deployment.</span></span>

## <span data-ttu-id="d951f-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d951f-110">EXAMPLES</span></span>

### <span data-ttu-id="d951f-111">Exemplo 1: reimplantar um site</span><span class="sxs-lookup"><span data-stu-id="d951f-111">Example 1: Redeploy a site</span></span>
```
PS C:\> Restore-AzureWebsiteDeployment -Name "ContosoSite" -CommitId "f876543210"
```

<span data-ttu-id="d951f-112">Esse comando reimplanta a implantação que tem a ID f876543210 para o site chamado ContosoSite.</span><span class="sxs-lookup"><span data-stu-id="d951f-112">This command redeploys the deployment that has the ID f876543210 for the website named ContosoSite.</span></span>

## <span data-ttu-id="d951f-113">OS</span><span class="sxs-lookup"><span data-stu-id="d951f-113">PARAMETERS</span></span>

### <span data-ttu-id="d951f-114">-Commitid</span><span class="sxs-lookup"><span data-stu-id="d951f-114">-CommitId</span></span>
<span data-ttu-id="d951f-115">Especifica o identificador da implantação a ser reimplantada.</span><span class="sxs-lookup"><span data-stu-id="d951f-115">Specifies the identifier of the deployment to redeploy.</span></span>

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

### <span data-ttu-id="d951f-116">-Force</span><span class="sxs-lookup"><span data-stu-id="d951f-116">-Force</span></span>
<span data-ttu-id="d951f-117">Se habilitada, reimplanta a implantação anterior sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="d951f-117">If enabled, redeploys the previous deployment without prompting for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d951f-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="d951f-118">-Name</span></span>
<span data-ttu-id="d951f-119">Especifica o nome do site a ser reimplantado.</span><span class="sxs-lookup"><span data-stu-id="d951f-119">Specifies the name of the website to redeploy.</span></span>

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

### <span data-ttu-id="d951f-120">-Perfil</span><span class="sxs-lookup"><span data-stu-id="d951f-120">-Profile</span></span>
<span data-ttu-id="d951f-121">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="d951f-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d951f-122">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="d951f-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d951f-123">-Slot</span><span class="sxs-lookup"><span data-stu-id="d951f-123">-Slot</span></span>
<span data-ttu-id="d951f-124">Especifica o nome do slot.</span><span class="sxs-lookup"><span data-stu-id="d951f-124">Specifies the slot name.</span></span>

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

### <span data-ttu-id="d951f-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d951f-125">-Confirm</span></span>
<span data-ttu-id="d951f-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d951f-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d951f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d951f-127">-WhatIf</span></span>
<span data-ttu-id="d951f-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d951f-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d951f-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d951f-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d951f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d951f-130">CommonParameters</span></span>
<span data-ttu-id="d951f-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d951f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d951f-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d951f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d951f-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d951f-133">INPUTS</span></span>

## <span data-ttu-id="d951f-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d951f-134">OUTPUTS</span></span>

## <span data-ttu-id="d951f-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d951f-135">NOTES</span></span>

## <span data-ttu-id="d951f-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d951f-136">RELATED LINKS</span></span>

[<span data-ttu-id="d951f-137">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="d951f-137">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="d951f-138">Get-AzureWebsiteDeployment</span><span class="sxs-lookup"><span data-stu-id="d951f-138">Get-AzureWebsiteDeployment</span></span>](./Get-AzureWebsiteDeployment.md)


