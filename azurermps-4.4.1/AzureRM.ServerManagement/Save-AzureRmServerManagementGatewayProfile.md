---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: ECF85C07-2C9E-487D-A2ED-77875C380244
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Save-AzureRmServerManagementGatewayProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Save-AzureRmServerManagementGatewayProfile.md
ms.openlocfilehash: af7184b3e43d2016ff4acc9e7634f831945a8fdf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433005"
---
# <span data-ttu-id="5936b-101">Save-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="5936b-101">Save-AzureRmServerManagementGatewayProfile</span></span>

## <span data-ttu-id="5936b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5936b-102">SYNOPSIS</span></span>
<span data-ttu-id="5936b-103">Baixa o perfil de um gateway de gerenciamento de servidor e salva-o em um arquivo local.</span><span class="sxs-lookup"><span data-stu-id="5936b-103">Downloads the profile for a Server Management gateway and saves it to a local file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5936b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5936b-104">SYNTAX</span></span>

### <span data-ttu-id="5936b-105">ByName</span><span class="sxs-lookup"><span data-stu-id="5936b-105">ByName</span></span>
```
Save-AzureRmServerManagementGatewayProfile [-OutputFile] <FileInfo> [-ResourceGroupName] <String>
 [-GatewayName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5936b-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="5936b-106">ByObject</span></span>
```
Save-AzureRmServerManagementGatewayProfile [-OutputFile] <FileInfo> [-Gateway] <Gateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5936b-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5936b-107">DESCRIPTION</span></span>
<span data-ttu-id="5936b-108">O cmdlet **Save-AzureRmServerManagementGatewayProfile** faz o download do perfil de um gateway de gerenciamento do servidor do Azure e o armazena em um arquivo local.</span><span class="sxs-lookup"><span data-stu-id="5936b-108">The **Save-AzureRmServerManagementGatewayProfile** cmdlet downloads the profile for an Azure Server Management gateway and stores it to a local file.</span></span>

## <span data-ttu-id="5936b-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5936b-109">EXAMPLES</span></span>

## <span data-ttu-id="5936b-110">OS</span><span class="sxs-lookup"><span data-stu-id="5936b-110">PARAMETERS</span></span>

### <span data-ttu-id="5936b-111">-Gateway</span><span class="sxs-lookup"><span data-stu-id="5936b-111">-Gateway</span></span>
<span data-ttu-id="5936b-112">Especifica o gateway para o qual esse cmdlet obtém o perfil.</span><span class="sxs-lookup"><span data-stu-id="5936b-112">Specifies the gateway that this cmdlet gets the profile for.</span></span>

<span data-ttu-id="5936b-113">Pode ser usado em vez de especificar ResourceGroupName e GATEWAYNAME</span><span class="sxs-lookup"><span data-stu-id="5936b-113">May be used instead of specifying ResourceGroupName and GatewayName</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServerManagement.Model.Gateway
Parameter Sets: ByObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5936b-114">-GATEWAYNAME</span><span class="sxs-lookup"><span data-stu-id="5936b-114">-GatewayName</span></span>
<span data-ttu-id="5936b-115">Especifica o nome do gateway para o qual esse cmdlet obtém o perfil.</span><span class="sxs-lookup"><span data-stu-id="5936b-115">Specifies the name of the gateway that this cmdlet gets the profile for.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5936b-116">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="5936b-116">-OutputFile</span></span>
<span data-ttu-id="5936b-117">Especifica o arquivo local no qual os dados do perfil são salvos.</span><span class="sxs-lookup"><span data-stu-id="5936b-117">Specifies the local file in which to save the profile data.</span></span>

```yaml
Type: System.IO.FileInfo
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5936b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5936b-118">-ResourceGroupName</span></span>
<span data-ttu-id="5936b-119">Especifica o nome do grupo de recursos ao qual o gateway pertence.</span><span class="sxs-lookup"><span data-stu-id="5936b-119">Specifies the name of the resource group that the gateway belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5936b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5936b-120">-DefaultProfile</span></span>
<span data-ttu-id="5936b-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5936b-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5936b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5936b-122">CommonParameters</span></span>
<span data-ttu-id="5936b-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5936b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5936b-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5936b-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5936b-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5936b-125">INPUTS</span></span>

### <span data-ttu-id="5936b-126">Gateway</span><span class="sxs-lookup"><span data-stu-id="5936b-126">Gateway</span></span>
<span data-ttu-id="5936b-127">O parâmetro ' gateway ' aceita o valor do tipo ' gateway ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="5936b-127">Parameter 'Gateway' accepts value of type 'Gateway' from the pipeline</span></span>

## <span data-ttu-id="5936b-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5936b-128">OUTPUTS</span></span>

### <span data-ttu-id="5936b-129">System. IO. FileInfo</span><span class="sxs-lookup"><span data-stu-id="5936b-129">System.IO.FileInfo</span></span>

## <span data-ttu-id="5936b-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5936b-130">NOTES</span></span>

## <span data-ttu-id="5936b-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5936b-131">RELATED LINKS</span></span>

[<span data-ttu-id="5936b-132">Install-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="5936b-132">Install-AzureRmServerManagementGatewayProfile</span></span>](./Install-AzureRmServerManagementGatewayProfile.md)

[<span data-ttu-id="5936b-133">Reset-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="5936b-133">Reset-AzureRmServerManagementGatewayProfile</span></span>](./Reset-AzureRmServerManagementGatewayProfile.md)


