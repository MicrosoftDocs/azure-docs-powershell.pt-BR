---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: 06081209-BBE5-4F76-86F8-9CF6197938F8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Install-AzureRmServerManagementGatewayProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Install-AzureRmServerManagementGatewayProfile.md
ms.openlocfilehash: b1d3d757d7970a21a2d81af9f1e08d0d8126df96
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602690"
---
# <span data-ttu-id="ab0a9-101">Install-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="ab0a9-101">Install-AzureRmServerManagementGatewayProfile</span></span>

## <span data-ttu-id="ab0a9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ab0a9-102">SYNOPSIS</span></span>
<span data-ttu-id="ab0a9-103">Instala um perfil do gateway de gerenciamento do servidor.</span><span class="sxs-lookup"><span data-stu-id="ab0a9-103">Installs a Server Management Gateway profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab0a9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ab0a9-104">SYNTAX</span></span>

```
Install-AzureRmServerManagementGatewayProfile [[-InputFile] <FileInfo>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab0a9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ab0a9-105">DESCRIPTION</span></span>
<span data-ttu-id="ab0a9-106">O cmdlet **install-AzureRmServerManagementGatewayProfile** instala um perfil do gateway de gerenciamento do servidor do Azure no local correto.</span><span class="sxs-lookup"><span data-stu-id="ab0a9-106">The **Install-AzureRmServerManagementGatewayProfile** cmdlet installs an Azure Server Management Gateway profile into the correct location.</span></span>
<span data-ttu-id="ab0a9-107">O arquivo que este cmdlet instala é chamado de profile.js.</span><span class="sxs-lookup"><span data-stu-id="ab0a9-107">The file that this cmdlet installs is named profile.json.</span></span>

## <span data-ttu-id="ab0a9-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ab0a9-108">EXAMPLES</span></span>

## <span data-ttu-id="ab0a9-109">OS</span><span class="sxs-lookup"><span data-stu-id="ab0a9-109">PARAMETERS</span></span>

### <span data-ttu-id="ab0a9-110">-InputFile</span><span class="sxs-lookup"><span data-stu-id="ab0a9-110">-InputFile</span></span>
<span data-ttu-id="ab0a9-111">Especifica o nome do arquivo local que contém o perfil do gateway a ser instalado.</span><span class="sxs-lookup"><span data-stu-id="ab0a9-111">Specifies the name of the local file that contains the gateway profile to install.</span></span>

<span data-ttu-id="ab0a9-112">O arquivo que esse cmdlet instala deve ter sido salvo anteriormente com o cmdlet Save-AzureRmServerManagementGatewayProfile.</span><span class="sxs-lookup"><span data-stu-id="ab0a9-112">The file that this cmdlet installs should have been previously saved with the Save-AzureRmServerManagementGatewayProfile cmdlet.</span></span>

```yaml
Type: System.IO.FileInfo
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ab0a9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab0a9-113">-DefaultProfile</span></span>
<span data-ttu-id="ab0a9-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ab0a9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab0a9-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab0a9-115">CommonParameters</span></span>
<span data-ttu-id="ab0a9-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab0a9-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab0a9-117">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab0a9-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab0a9-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ab0a9-118">INPUTS</span></span>

### <span data-ttu-id="ab0a9-119">Method</span><span class="sxs-lookup"><span data-stu-id="ab0a9-119">FileInfo</span></span>
<span data-ttu-id="ab0a9-120">O parâmetro ' InputFile ' aceita o valor do tipo ' FileInfo ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="ab0a9-120">Parameter 'InputFile' accepts value of type 'FileInfo' from the pipeline</span></span>

## <span data-ttu-id="ab0a9-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ab0a9-121">OUTPUTS</span></span>

## <span data-ttu-id="ab0a9-122">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ab0a9-122">NOTES</span></span>

## <span data-ttu-id="ab0a9-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ab0a9-123">RELATED LINKS</span></span>

[<span data-ttu-id="ab0a9-124">Reset-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="ab0a9-124">Reset-AzureRmServerManagementGatewayProfile</span></span>](./Reset-AzureRmServerManagementGatewayProfile.md)

[<span data-ttu-id="ab0a9-125">Save-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="ab0a9-125">Save-AzureRmServerManagementGatewayProfile</span></span>](./Save-AzureRmServerManagementGatewayProfile.md)


