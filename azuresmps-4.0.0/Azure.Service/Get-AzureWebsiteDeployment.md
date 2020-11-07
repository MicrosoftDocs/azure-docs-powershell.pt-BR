---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D15329E9-BB72-4F1B-B79A-E7AD920A9D5A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 92c972bb693a1e13b365635064785182c53af409
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946509"
---
# <span data-ttu-id="e10e3-101">Get-AzureWebsiteDeployment</span><span class="sxs-lookup"><span data-stu-id="e10e3-101">Get-AzureWebsiteDeployment</span></span>

## <span data-ttu-id="e10e3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e10e3-102">SYNOPSIS</span></span>
<span data-ttu-id="e10e3-103">Obtém as implantações para um site.</span><span class="sxs-lookup"><span data-stu-id="e10e3-103">Gets the deployments for a website.</span></span>

## <span data-ttu-id="e10e3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e10e3-104">SYNTAX</span></span>

```
Get-AzureWebsiteDeployment [-CommitId <String>] [-MaxResults <Int32>] [-Details] [-Name <String>]
 [-Slot <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e10e3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e10e3-105">DESCRIPTION</span></span>
<span data-ttu-id="e10e3-106">Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e10e3-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="e10e3-107">Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="e10e3-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="e10e3-108">Obtém as implantações para um site no Azure.</span><span class="sxs-lookup"><span data-stu-id="e10e3-108">Gets the deployments for a website in Azure.</span></span>

## <span data-ttu-id="e10e3-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e10e3-109">EXAMPLES</span></span>

## <span data-ttu-id="e10e3-110">OS</span><span class="sxs-lookup"><span data-stu-id="e10e3-110">PARAMETERS</span></span>

### <span data-ttu-id="e10e3-111">-Commitid</span><span class="sxs-lookup"><span data-stu-id="e10e3-111">-CommitId</span></span>
<span data-ttu-id="e10e3-112">Especifica a ID exclusiva para a implantação.</span><span class="sxs-lookup"><span data-stu-id="e10e3-112">Specifies the unique ID for the deployment.</span></span>

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

### <span data-ttu-id="e10e3-113">-Detalhes</span><span class="sxs-lookup"><span data-stu-id="e10e3-113">-Details</span></span>
<span data-ttu-id="e10e3-114">Mostra informações detalhadas sobre as implantações.</span><span class="sxs-lookup"><span data-stu-id="e10e3-114">Shows detailed information about the deployments.</span></span>

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

### <span data-ttu-id="e10e3-115">-MaxResults</span><span class="sxs-lookup"><span data-stu-id="e10e3-115">-MaxResults</span></span>
<span data-ttu-id="e10e3-116">Especifica o maior número de resultados que você deseja que o comando retorne.</span><span class="sxs-lookup"><span data-stu-id="e10e3-116">Specifies the largest number of results that you want the command to return.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e10e3-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="e10e3-117">-Name</span></span>
<span data-ttu-id="e10e3-118">Especifica o nome do site para o qual você deseja obter informações sobre a implantação.</span><span class="sxs-lookup"><span data-stu-id="e10e3-118">Specifies the name of the website for which you want to get deployment information.</span></span>

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

### <span data-ttu-id="e10e3-119">-Perfil</span><span class="sxs-lookup"><span data-stu-id="e10e3-119">-Profile</span></span>
<span data-ttu-id="e10e3-120">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="e10e3-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e10e3-121">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="e10e3-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e10e3-122">-Slot</span><span class="sxs-lookup"><span data-stu-id="e10e3-122">-Slot</span></span>
<span data-ttu-id="e10e3-123">Especifica o nome do slot.</span><span class="sxs-lookup"><span data-stu-id="e10e3-123">Specifies the slot name.</span></span>

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

### <span data-ttu-id="e10e3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e10e3-124">CommonParameters</span></span>
<span data-ttu-id="e10e3-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e10e3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e10e3-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e10e3-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e10e3-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e10e3-127">INPUTS</span></span>

## <span data-ttu-id="e10e3-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e10e3-128">OUTPUTS</span></span>

## <span data-ttu-id="e10e3-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e10e3-129">NOTES</span></span>

## <span data-ttu-id="e10e3-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e10e3-130">RELATED LINKS</span></span>

[<span data-ttu-id="e10e3-131">Restore-AzureWebsiteDeployment</span><span class="sxs-lookup"><span data-stu-id="e10e3-131">Restore-AzureWebsiteDeployment</span></span>](./Restore-AzureWebsiteDeployment.md)


