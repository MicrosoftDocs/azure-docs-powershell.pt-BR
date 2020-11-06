---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 2D83D38F-3A5C-40DB-BE8B-D52E5CAFCF6E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppCertificate.md
ms.openlocfilehash: 94cd9c6aa3c47d87b1c99a1f8ae68c48c613aefd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429275"
---
# <span data-ttu-id="a6500-101">Get-AzureRmWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="a6500-101">Get-AzureRmWebAppCertificate</span></span>

## <span data-ttu-id="a6500-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a6500-102">SYNOPSIS</span></span>
<span data-ttu-id="a6500-103">Obtém um certificado do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="a6500-103">Gets an Azure Web App certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a6500-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a6500-104">SYNTAX</span></span>

```
Get-AzureRmWebAppCertificate [[-ResourceGroupName] <String>] [[-Thumbprint] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a6500-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a6500-105">DESCRIPTION</span></span>
<span data-ttu-id="a6500-106">O cmdlet **Get-AzureRmWebAppCertificate** Obtém informações sobre os certificados do Azure Web App associados a um grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="a6500-106">The **Get-AzureRmWebAppCertificate** cmdlet gets information about Azure Web App certificates associated with a specified resource group.</span></span>
<span data-ttu-id="a6500-107">Se você souber a impressão digital do certificado, também poderá usar esse cmdlet para obter informações sobre um certificado especificado.</span><span class="sxs-lookup"><span data-stu-id="a6500-107">If you know the certificate thumbprint you can also use this cmdlet to get information about a specified certificate.</span></span>

## <span data-ttu-id="a6500-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a6500-108">EXAMPLES</span></span>

### <span data-ttu-id="a6500-109">Exemplo 1: obter certificados do aplicativo Web em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="a6500-109">Example 1: Get Web App certificates in a resource group</span></span>
```
PS C:\>Get-AzureRmWebAppCertificate -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="a6500-110">Esse comando retorna informações sobre os certificados do aplicativo Web carregados associados à ContosoResourceGroup do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a6500-110">This command returns information about the uploaded Web App certificates associated with the resource group ContosoResourceGroup.</span></span>

### <span data-ttu-id="a6500-111">Exemplo 2: obter um certificado de aplicativo Web especificado</span><span class="sxs-lookup"><span data-stu-id="a6500-111">Example 2: Get a specified web app certificate</span></span>
```
PS C:\>Get-AzureRmWebAppCertificate -ResourceGroupName "ContosoResourceGroup" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="a6500-112">Esse comando obtém o certificado do aplicativo Web ContosoResourceGroup com o E3A38EBA60CAA1C162785A2E1C44A15AD450199C3 de impressão digital.</span><span class="sxs-lookup"><span data-stu-id="a6500-112">This command gets the ContosoResourceGroup Web App certificate with the thumbprint E3A38EBA60CAA1C162785A2E1C44A15AD450199C3.</span></span>

## <span data-ttu-id="a6500-113">OS</span><span class="sxs-lookup"><span data-stu-id="a6500-113">PARAMETERS</span></span>

### <span data-ttu-id="a6500-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6500-114">-DefaultProfile</span></span>
<span data-ttu-id="a6500-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a6500-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6500-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6500-116">-ResourceGroupName</span></span>
<span data-ttu-id="a6500-117">Especifica o nome do grupo de recursos ao qual o certificado está atribuído.</span><span class="sxs-lookup"><span data-stu-id="a6500-117">Specifies the name of the resource group that the certificate is assigned to.</span></span>

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

### <span data-ttu-id="a6500-118">-Impressão digital</span><span class="sxs-lookup"><span data-stu-id="a6500-118">-Thumbprint</span></span>
<span data-ttu-id="a6500-119">Especifica o identificador exclusivo do certificado.</span><span class="sxs-lookup"><span data-stu-id="a6500-119">Specifies the unique identifier for the certificate.</span></span>

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

### <span data-ttu-id="a6500-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6500-120">CommonParameters</span></span>
<span data-ttu-id="a6500-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6500-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6500-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6500-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6500-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a6500-123">INPUTS</span></span>

### <span data-ttu-id="a6500-124">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="a6500-124">None</span></span>

## <span data-ttu-id="a6500-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a6500-125">OUTPUTS</span></span>

### <span data-ttu-id="a6500-126">Microsoft. Azure. Management. WebSites. Models. Certificate</span><span class="sxs-lookup"><span data-stu-id="a6500-126">Microsoft.Azure.Management.WebSites.Models.Certificate</span></span>

## <span data-ttu-id="a6500-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a6500-127">NOTES</span></span>

## <span data-ttu-id="a6500-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a6500-128">RELATED LINKS</span></span>

[<span data-ttu-id="a6500-129">Get-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="a6500-129">Get-AzureRmWebAppSSLBinding</span></span>](./Get-AzureRmWebAppSSLBinding.md)

