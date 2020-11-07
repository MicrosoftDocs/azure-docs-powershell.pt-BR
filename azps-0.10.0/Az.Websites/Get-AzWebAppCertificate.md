---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 2D83D38F-3A5C-40DB-BE8B-D52E5CAFCF6E
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebappcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppCertificate.md
ms.openlocfilehash: f06075a8067ae8a7d7e1c2dcd522774325b48c57
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776117"
---
# <span data-ttu-id="12361-101">Get-AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="12361-101">Get-AzWebAppCertificate</span></span>

## <span data-ttu-id="12361-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="12361-102">SYNOPSIS</span></span>
<span data-ttu-id="12361-103">Obtém um certificado do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="12361-103">Gets an Azure Web App certificate.</span></span>

## <span data-ttu-id="12361-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="12361-104">SYNTAX</span></span>

```
Get-AzWebAppCertificate [[-ResourceGroupName] <String>] [[-Thumbprint] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12361-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="12361-105">DESCRIPTION</span></span>
<span data-ttu-id="12361-106">O cmdlet **Get-AzWebAppCertificate** Obtém informações sobre os certificados do Azure Web App associados a um grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="12361-106">The **Get-AzWebAppCertificate** cmdlet gets information about Azure Web App certificates associated with a specified resource group.</span></span>
<span data-ttu-id="12361-107">Se você souber a impressão digital do certificado, também poderá usar esse cmdlet para obter informações sobre um certificado especificado.</span><span class="sxs-lookup"><span data-stu-id="12361-107">If you know the certificate thumbprint you can also use this cmdlet to get information about a specified certificate.</span></span>

## <span data-ttu-id="12361-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="12361-108">EXAMPLES</span></span>

### <span data-ttu-id="12361-109">Exemplo 1: obter certificados do aplicativo Web em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="12361-109">Example 1: Get Web App certificates in a resource group</span></span>
```
PS C:\>Get-AzWebAppCertificate -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="12361-110">Esse comando retorna informações sobre os certificados do aplicativo Web carregados associados à ContosoResourceGroup do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="12361-110">This command returns information about the uploaded Web App certificates associated with the resource group ContosoResourceGroup.</span></span>

### <span data-ttu-id="12361-111">Exemplo 2: obter um certificado de aplicativo Web especificado</span><span class="sxs-lookup"><span data-stu-id="12361-111">Example 2: Get a specified web app certificate</span></span>
```
PS C:\>Get-AzWebAppCertificate -ResourceGroupName "ContosoResourceGroup" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="12361-112">Esse comando obtém o certificado do aplicativo Web ContosoResourceGroup com o E3A38EBA60CAA1C162785A2E1C44A15AD450199C3 de impressão digital.</span><span class="sxs-lookup"><span data-stu-id="12361-112">This command gets the ContosoResourceGroup Web App certificate with the thumbprint E3A38EBA60CAA1C162785A2E1C44A15AD450199C3.</span></span>

## <span data-ttu-id="12361-113">OS</span><span class="sxs-lookup"><span data-stu-id="12361-113">PARAMETERS</span></span>

### <span data-ttu-id="12361-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12361-114">-DefaultProfile</span></span>
<span data-ttu-id="12361-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="12361-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="12361-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12361-116">-ResourceGroupName</span></span>
<span data-ttu-id="12361-117">Especifica o nome do grupo de recursos ao qual o certificado está atribuído.</span><span class="sxs-lookup"><span data-stu-id="12361-117">Specifies the name of the resource group that the certificate is assigned to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12361-118">-Impressão digital</span><span class="sxs-lookup"><span data-stu-id="12361-118">-Thumbprint</span></span>
<span data-ttu-id="12361-119">Especifica o identificador exclusivo do certificado.</span><span class="sxs-lookup"><span data-stu-id="12361-119">Specifies the unique identifier for the certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12361-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12361-120">CommonParameters</span></span>
<span data-ttu-id="12361-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12361-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12361-122">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12361-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12361-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="12361-123">INPUTS</span></span>

### <span data-ttu-id="12361-124">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="12361-124">None</span></span>
<span data-ttu-id="12361-125">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="12361-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="12361-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="12361-126">OUTPUTS</span></span>

## <span data-ttu-id="12361-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="12361-127">NOTES</span></span>

## <span data-ttu-id="12361-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="12361-128">RELATED LINKS</span></span>

[<span data-ttu-id="12361-129">Get-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="12361-129">Get-AzWebAppSSLBinding</span></span>](./Get-AzWebAppSSLBinding.md)


