---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-AzWebAppCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppCertificate.md
ms.openlocfilehash: 7988975daa512b44c71b17929f47d3318bfe192c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112325"
---
# <span data-ttu-id="985e3-101">Remove-AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="985e3-101">Remove-AzWebAppCertificate</span></span>

## <span data-ttu-id="985e3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="985e3-102">SYNOPSIS</span></span>
<span data-ttu-id="985e3-103">Cria um certificado gerenciado pelo serviço de aplicativos para um Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="985e3-103">Creates an App service managed certificate for an Azure Web App.</span></span> 

## <span data-ttu-id="985e3-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="985e3-104">SYNTAX</span></span>

```
Remove-AzWebAppCertificate [-ResourceGroupName] <String> [-ThumbPrint] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="985e3-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="985e3-105">DESCRIPTION</span></span>
<span data-ttu-id="985e3-106">O cmdlet **Remove-AzWebAppCertificate** cria um Certificado Gerenciado pelo Serviço do Azure App</span><span class="sxs-lookup"><span data-stu-id="985e3-106">The **Remove-AzWebAppCertificate** cmdlet creates an Azure App Service Managed Certificate</span></span>

## <span data-ttu-id="985e3-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="985e3-107">EXAMPLES</span></span>

### <span data-ttu-id="985e3-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="985e3-108">Example 1</span></span>
```powershell
PS C:\>Remove-AzWebAppCertificate -ResourceGroupName Default-Web-WestUS -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" 
```

<span data-ttu-id="985e3-109">Este comando remove o certificado gerenciado pelo serviço de aplicativo para o aplicativo Web determinado.</span><span class="sxs-lookup"><span data-stu-id="985e3-109">This command removes App Service Managed certificate for the given web app.</span></span>

## <span data-ttu-id="985e3-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="985e3-110">PARAMETERS</span></span>

### <span data-ttu-id="985e3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="985e3-111">-DefaultProfile</span></span>
<span data-ttu-id="985e3-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="985e3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="985e3-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="985e3-113">-ResourceGroupName</span></span>
<span data-ttu-id="985e3-114">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="985e3-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="985e3-115">-ThumbPrint</span><span class="sxs-lookup"><span data-stu-id="985e3-115">-ThumbPrint</span></span>
<span data-ttu-id="985e3-116">Impressão digital do certificado que já existe no espaço da Web.</span><span class="sxs-lookup"><span data-stu-id="985e3-116">Thumbprint of the certificate that already exists in web space.</span></span>

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

### <span data-ttu-id="985e3-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="985e3-117">CommonParameters</span></span>
<span data-ttu-id="985e3-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="985e3-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="985e3-119">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="985e3-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="985e3-120">Entradas</span><span class="sxs-lookup"><span data-stu-id="985e3-120">INPUTS</span></span>

### <span data-ttu-id="985e3-121">Nenhum</span><span class="sxs-lookup"><span data-stu-id="985e3-121">None</span></span>

## <span data-ttu-id="985e3-122">Saídas</span><span class="sxs-lookup"><span data-stu-id="985e3-122">OUTPUTS</span></span>

### <span data-ttu-id="985e3-123">System.Void</span><span class="sxs-lookup"><span data-stu-id="985e3-123">System.Void</span></span>

## <span data-ttu-id="985e3-124">Notas</span><span class="sxs-lookup"><span data-stu-id="985e3-124">NOTES</span></span>

## <span data-ttu-id="985e3-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="985e3-125">RELATED LINKS</span></span>
[<span data-ttu-id="985e3-126">New-AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="985e3-126">New-AzWebAppCertificate</span></span>](./New-AzWebAppCertificate.md)
