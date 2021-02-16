---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 2D83D38F-3A5C-40DB-BE8B-D52E5CAFCF6E
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppCertificate.md
ms.openlocfilehash: e348d29a805de900aa3144832084e657cf85077c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118510"
---
# <span data-ttu-id="ca80f-101">Get-AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="ca80f-101">Get-AzWebAppCertificate</span></span>

## <span data-ttu-id="ca80f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ca80f-102">SYNOPSIS</span></span>
<span data-ttu-id="ca80f-103">Recebe um certificado do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="ca80f-103">Gets an Azure Web App certificate.</span></span>

## <span data-ttu-id="ca80f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ca80f-104">SYNTAX</span></span>

```
Get-AzWebAppCertificate [[-ResourceGroupName] <String>] [[-Thumbprint] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ca80f-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="ca80f-105">DESCRIPTION</span></span>
<span data-ttu-id="ca80f-106">O cmdlet **Get-AzWebAppCertificate** obtém informações sobre certificados do Azure Web App associados a um grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="ca80f-106">The **Get-AzWebAppCertificate** cmdlet gets information about Azure Web App certificates associated with a specified resource group.</span></span>
<span data-ttu-id="ca80f-107">Se você sabe a miniatura do certificado, também pode usar esse cmdlet para obter informações sobre um certificado especificado.</span><span class="sxs-lookup"><span data-stu-id="ca80f-107">If you know the certificate thumbprint you can also use this cmdlet to get information about a specified certificate.</span></span>

## <span data-ttu-id="ca80f-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ca80f-108">EXAMPLES</span></span>

### <span data-ttu-id="ca80f-109">Exemplo 1: Obter certificados do Web App em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="ca80f-109">Example 1: Get Web App certificates in a resource group</span></span>
```
PS C:\>Get-AzWebAppCertificate -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="ca80f-110">Esse comando retorna informações sobre os certificados do Web App carregados associados ao grupo de recursos ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="ca80f-110">This command returns information about the uploaded Web App certificates associated with the resource group ContosoResourceGroup.</span></span>

### <span data-ttu-id="ca80f-111">Exemplo 2: Obter um certificado de aplicativo Web especificado</span><span class="sxs-lookup"><span data-stu-id="ca80f-111">Example 2: Get a specified web app certificate</span></span>
```
PS C:\>Get-AzWebAppCertificate -ResourceGroupName "ContosoResourceGroup" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="ca80f-112">Esse comando obtém o certificado ContosoResourceGroup Web App com a impressão digital E3A38EBA60CAA1C162785A2E1C44A15AD450199C3.</span><span class="sxs-lookup"><span data-stu-id="ca80f-112">This command gets the ContosoResourceGroup Web App certificate with the thumbprint E3A38EBA60CAA1C162785A2E1C44A15AD450199C3.</span></span>

## <span data-ttu-id="ca80f-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ca80f-113">PARAMETERS</span></span>

### <span data-ttu-id="ca80f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca80f-114">-DefaultProfile</span></span>
<span data-ttu-id="ca80f-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="ca80f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ca80f-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca80f-116">-ResourceGroupName</span></span>
<span data-ttu-id="ca80f-117">Especifica o nome do grupo de recursos ao que o certificado foi atribuído.</span><span class="sxs-lookup"><span data-stu-id="ca80f-117">Specifies the name of the resource group that the certificate is assigned to.</span></span>

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

### <span data-ttu-id="ca80f-118">-Impressão digital</span><span class="sxs-lookup"><span data-stu-id="ca80f-118">-Thumbprint</span></span>
<span data-ttu-id="ca80f-119">Especifica o identificador exclusivo do certificado.</span><span class="sxs-lookup"><span data-stu-id="ca80f-119">Specifies the unique identifier for the certificate.</span></span>

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

### <span data-ttu-id="ca80f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca80f-120">CommonParameters</span></span>
<span data-ttu-id="ca80f-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca80f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca80f-122">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca80f-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca80f-123">Entradas</span><span class="sxs-lookup"><span data-stu-id="ca80f-123">INPUTS</span></span>

### <span data-ttu-id="ca80f-124">Nenhum</span><span class="sxs-lookup"><span data-stu-id="ca80f-124">None</span></span>

## <span data-ttu-id="ca80f-125">Saídas</span><span class="sxs-lookup"><span data-stu-id="ca80f-125">OUTPUTS</span></span>

### <span data-ttu-id="ca80f-126">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSCertificate</span><span class="sxs-lookup"><span data-stu-id="ca80f-126">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSCertificate</span></span>

## <span data-ttu-id="ca80f-127">Notas</span><span class="sxs-lookup"><span data-stu-id="ca80f-127">NOTES</span></span>

## <span data-ttu-id="ca80f-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ca80f-128">RELATED LINKS</span></span>

[<span data-ttu-id="ca80f-129">Get-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="ca80f-129">Get-AzWebAppSSLBinding</span></span>](./Get-AzWebAppSSLBinding.md)


