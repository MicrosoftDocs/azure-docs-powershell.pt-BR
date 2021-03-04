---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 2D83D38F-3A5C-40DB-BE8B-D52E5CAFCF6E
online version: https://docs.microsoft.com/powershell/module/az.websites/get-azwebappcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppCertificate.md
ms.openlocfilehash: 12603400c3d1f29eaf77d9a279d7510e08b9fe5d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890683"
---
# <span data-ttu-id="0a753-101">Get-AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="0a753-101">Get-AzWebAppCertificate</span></span>

## <span data-ttu-id="0a753-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a753-102">SYNOPSIS</span></span>
<span data-ttu-id="0a753-103">Obtém um certificado do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="0a753-103">Gets an Azure Web App certificate.</span></span>

## <span data-ttu-id="0a753-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="0a753-104">SYNTAX</span></span>

```
Get-AzWebAppCertificate [[-ResourceGroupName] <String>] [[-Thumbprint] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a753-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="0a753-105">DESCRIPTION</span></span>
<span data-ttu-id="0a753-106">O cmdlet **Get-AzWebAppCertificate** obtém informações sobre certificados do Azure Web App associados a um grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="0a753-106">The **Get-AzWebAppCertificate** cmdlet gets information about Azure Web App certificates associated with a specified resource group.</span></span>
<span data-ttu-id="0a753-107">Se você conhece a impressão digital do certificado, também pode usar esse cmdlet para obter informações sobre um certificado especificado.</span><span class="sxs-lookup"><span data-stu-id="0a753-107">If you know the certificate thumbprint you can also use this cmdlet to get information about a specified certificate.</span></span>

## <span data-ttu-id="0a753-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0a753-108">EXAMPLES</span></span>

### <span data-ttu-id="0a753-109">Exemplo 1: Obter certificados do Aplicativo Web em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="0a753-109">Example 1: Get Web App certificates in a resource group</span></span>
```
PS C:\>Get-AzWebAppCertificate -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="0a753-110">Este comando retorna informações sobre os certificados do Aplicativo Web carregados associados ao grupo de recursos ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="0a753-110">This command returns information about the uploaded Web App certificates associated with the resource group ContosoResourceGroup.</span></span>

### <span data-ttu-id="0a753-111">Exemplo 2: Obter um certificado de aplicativo Web especificado</span><span class="sxs-lookup"><span data-stu-id="0a753-111">Example 2: Get a specified web app certificate</span></span>
```
PS C:\>Get-AzWebAppCertificate -ResourceGroupName "ContosoResourceGroup" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="0a753-112">Este comando obtém o certificado do Aplicativo Web ContosoResourceGroup com a impressão digital E3A38EBA60CAA1C162785A2E1C44A15AD450199C3.</span><span class="sxs-lookup"><span data-stu-id="0a753-112">This command gets the ContosoResourceGroup Web App certificate with the thumbprint E3A38EBA60CAA1C162785A2E1C44A15AD450199C3.</span></span>

## <span data-ttu-id="0a753-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="0a753-113">PARAMETERS</span></span>

### <span data-ttu-id="0a753-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a753-114">-DefaultProfile</span></span>
<span data-ttu-id="0a753-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="0a753-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a753-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a753-116">-ResourceGroupName</span></span>
<span data-ttu-id="0a753-117">Especifica o nome do grupo de recursos ao que o certificado é atribuído.</span><span class="sxs-lookup"><span data-stu-id="0a753-117">Specifies the name of the resource group that the certificate is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a753-118">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="0a753-118">-Thumbprint</span></span>
<span data-ttu-id="0a753-119">Especifica o identificador exclusivo do certificado.</span><span class="sxs-lookup"><span data-stu-id="0a753-119">Specifies the unique identifier for the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a753-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a753-120">CommonParameters</span></span>
<span data-ttu-id="0a753-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a753-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a753-122">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a753-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a753-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0a753-123">INPUTS</span></span>

### <span data-ttu-id="0a753-124">Nenhum</span><span class="sxs-lookup"><span data-stu-id="0a753-124">None</span></span>

## <span data-ttu-id="0a753-125">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="0a753-125">OUTPUTS</span></span>

### <span data-ttu-id="0a753-126">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSCertificate</span><span class="sxs-lookup"><span data-stu-id="0a753-126">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSCertificate</span></span>

## <span data-ttu-id="0a753-127">NOTES</span><span class="sxs-lookup"><span data-stu-id="0a753-127">NOTES</span></span>

## <span data-ttu-id="0a753-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0a753-128">RELATED LINKS</span></span>

[<span data-ttu-id="0a753-129">Get-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="0a753-129">Get-AzWebAppSSLBinding</span></span>](./Get-AzWebAppSSLBinding.md)


