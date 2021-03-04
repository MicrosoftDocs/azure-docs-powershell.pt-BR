---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/remove-AzWebAppCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppCertificate.md
ms.openlocfilehash: adea8ace20b5e7c3c3c8d28161de53afdb431e19
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889101"
---
# <span data-ttu-id="ffe28-101">Remove-AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="ffe28-101">Remove-AzWebAppCertificate</span></span>

## <span data-ttu-id="ffe28-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ffe28-102">SYNOPSIS</span></span>
<span data-ttu-id="ffe28-103">Remove um certificado gerenciado do serviço de aplicativo para um Aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="ffe28-103">Removes an App service managed certificate for an Azure Web App.</span></span> 

## <span data-ttu-id="ffe28-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ffe28-104">SYNTAX</span></span>

```
Remove-AzWebAppCertificate [-ResourceGroupName] <String> [-ThumbPrint] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ffe28-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ffe28-105">DESCRIPTION</span></span>
<span data-ttu-id="ffe28-106">O cmdlet **Remove-AzWebAppCertificate** Removes an Azure App Service Managed Certificate</span><span class="sxs-lookup"><span data-stu-id="ffe28-106">The **Remove-AzWebAppCertificate** cmdlet Removes an Azure App Service Managed Certificate</span></span>

## <span data-ttu-id="ffe28-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ffe28-107">EXAMPLES</span></span>

### <span data-ttu-id="ffe28-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ffe28-108">Example 1</span></span>
```powershell
PS C:\>Remove-AzWebAppCertificate -ResourceGroupName Default-Web-WestUS -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" 
```

<span data-ttu-id="ffe28-109">Este comando remove o certificado Gerenciado do Serviço de Aplicativo para o determinado aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="ffe28-109">This command removes App Service Managed certificate for the given web app.</span></span>

## <span data-ttu-id="ffe28-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ffe28-110">PARAMETERS</span></span>

### <span data-ttu-id="ffe28-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffe28-111">-DefaultProfile</span></span>
<span data-ttu-id="ffe28-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ffe28-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffe28-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffe28-113">-ResourceGroupName</span></span>
<span data-ttu-id="ffe28-114">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ffe28-114">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffe28-115">-ThumbPrint</span><span class="sxs-lookup"><span data-stu-id="ffe28-115">-ThumbPrint</span></span>
<span data-ttu-id="ffe28-116">Impressão digital do certificado que já existe no espaço da Web.</span><span class="sxs-lookup"><span data-stu-id="ffe28-116">Thumbprint of the certificate that already exists in web space.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffe28-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffe28-117">CommonParameters</span></span>
<span data-ttu-id="ffe28-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ffe28-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffe28-119">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ffe28-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffe28-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ffe28-120">INPUTS</span></span>

### <span data-ttu-id="ffe28-121">Nenhum</span><span class="sxs-lookup"><span data-stu-id="ffe28-121">None</span></span>

## <span data-ttu-id="ffe28-122">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ffe28-122">OUTPUTS</span></span>

### <span data-ttu-id="ffe28-123">System.Void</span><span class="sxs-lookup"><span data-stu-id="ffe28-123">System.Void</span></span>

## <span data-ttu-id="ffe28-124">NOTES</span><span class="sxs-lookup"><span data-stu-id="ffe28-124">NOTES</span></span>

## <span data-ttu-id="ffe28-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ffe28-125">RELATED LINKS</span></span>
[<span data-ttu-id="ffe28-126">New-AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="ffe28-126">New-AzWebAppCertificate</span></span>](./New-AzWebAppCertificate.md)
