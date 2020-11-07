---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: EF2D377C-C000-4BCA-8EB9-58C805FA5C31
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebappslotconfigname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSlotConfigName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSlotConfigName.md
ms.openlocfilehash: 414e25840b03127bbe94586248641e103c1f7d88
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776104"
---
# <span data-ttu-id="e3b74-101">Get-AzWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="e3b74-101">Get-AzWebAppSlotConfigName</span></span>

## <span data-ttu-id="e3b74-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e3b74-102">SYNOPSIS</span></span>
<span data-ttu-id="e3b74-103">Obter a lista de nomes de configuração de slots do aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="e3b74-103">Get the list of Web App Slot Config names</span></span>

## <span data-ttu-id="e3b74-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e3b74-104">SYNTAX</span></span>

### <span data-ttu-id="e3b74-105">Eles</span><span class="sxs-lookup"><span data-stu-id="e3b74-105">S1</span></span>
```
Get-AzWebAppSlotConfigName [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e3b74-106">S2</span><span class="sxs-lookup"><span data-stu-id="e3b74-106">S2</span></span>
```
Get-AzWebAppSlotConfigName [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e3b74-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e3b74-107">DESCRIPTION</span></span>
<span data-ttu-id="e3b74-108">O cmdlet **Get-AzWebAppSlotConfigName** recupera a lista de configurações do aplicativo e nomes de cadeias de conexão que estão marcados atualmente como configurações de slot</span><span class="sxs-lookup"><span data-stu-id="e3b74-108">The **Get-AzWebAppSlotConfigName** cmdlet retrieves the list of App Setting and Connection String names that are currently marked as slot settings</span></span>

## <span data-ttu-id="e3b74-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e3b74-109">EXAMPLES</span></span>

### <span data-ttu-id="e3b74-110">1:</span><span class="sxs-lookup"><span data-stu-id="e3b74-110">1:</span></span>
```
PS C:\>Get-AzWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="e3b74-111">Este comando obtém as configurações do aplicativo e cadeias de conexão pertinentes ao aplicativo Web chamado ContosoSite associado ao grupo de recursos padrão-Web-Oesteus</span><span class="sxs-lookup"><span data-stu-id="e3b74-111">This command gets App Settings and Connection strings pertaining to the Web App named ContosoSite associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="e3b74-112">OS</span><span class="sxs-lookup"><span data-stu-id="e3b74-112">PARAMETERS</span></span>

### <span data-ttu-id="e3b74-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3b74-113">-DefaultProfile</span></span>
<span data-ttu-id="e3b74-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e3b74-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3b74-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="e3b74-115">-Name</span></span>
<span data-ttu-id="e3b74-116">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="e3b74-116">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3b74-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3b74-117">-ResourceGroupName</span></span>
<span data-ttu-id="e3b74-118">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="e3b74-118">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3b74-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="e3b74-119">-WebApp</span></span>
<span data-ttu-id="e3b74-120">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="e3b74-120">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3b74-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3b74-121">CommonParameters</span></span>
<span data-ttu-id="e3b74-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3b74-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3b74-123">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3b74-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3b74-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e3b74-124">INPUTS</span></span>

### <span data-ttu-id="e3b74-125">Instalação</span><span class="sxs-lookup"><span data-stu-id="e3b74-125">Site</span></span>
<span data-ttu-id="e3b74-126">O parâmetro ' WebApp ' aceita o valor do tipo ' site ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="e3b74-126">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="e3b74-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e3b74-127">OUTPUTS</span></span>

## <span data-ttu-id="e3b74-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e3b74-128">NOTES</span></span>

## <span data-ttu-id="e3b74-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e3b74-129">RELATED LINKS</span></span>

