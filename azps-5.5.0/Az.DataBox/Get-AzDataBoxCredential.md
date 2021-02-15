---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/en-us/powershell/module/az.databox/get-azdataboxcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Get-AzDataBoxCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Get-AzDataBoxCredential.md
ms.openlocfilehash: 308f7aa185350635815622ed684e47ebea349f9f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112001"
---
# <span data-ttu-id="a5a35-101">Get-AzDataBoxCredential</span><span class="sxs-lookup"><span data-stu-id="a5a35-101">Get-AzDataBoxCredential</span></span>

## <span data-ttu-id="a5a35-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a5a35-102">SYNOPSIS</span></span>
<span data-ttu-id="a5a35-103">Obtém as credenciais da caixa de dados de um trabalho específico</span><span class="sxs-lookup"><span data-stu-id="a5a35-103">Gets the databox credentials of a specific job</span></span>

## <span data-ttu-id="a5a35-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a5a35-104">SYNTAX</span></span>

### <span data-ttu-id="a5a35-105">GetByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a5a35-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzDataBoxCredential -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a5a35-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5a35-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5a35-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="a5a35-107">DESCRIPTION</span></span>
<span data-ttu-id="a5a35-108">O cmdlet **Get-AzDataBoxCredential** obtém as credenciais da caixa de dados de um trabalho específico.</span><span class="sxs-lookup"><span data-stu-id="a5a35-108">The **Get-AzDataBoxCredential** cmdlet gets the credentials of the databox of a specific job.</span></span> <span data-ttu-id="a5a35-109">As propriedades internas do objeto de credenciais retornadas serão diferentes para diferentes tipos de SKU.</span><span class="sxs-lookup"><span data-stu-id="a5a35-109">The internal properties of the returned credentials object will be different for different Sku types.</span></span>

## <span data-ttu-id="a5a35-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a5a35-110">EXAMPLES</span></span>

### <span data-ttu-id="a5a35-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a5a35-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxCredential -ResourceGroupName TestRg1 -Name TestJob1

JobName     JobSecrets
-------     ----------
TestJob1    Microsoft.Azure.Management.DataBox.Models.DataboxJobSecrets
```

<span data-ttu-id="a5a35-112">Isso reajusta os JobSecsecsecs do trabalho especificado</span><span class="sxs-lookup"><span data-stu-id="a5a35-112">This retuns the JobSecrets of the specified job</span></span>

### <span data-ttu-id="a5a35-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="a5a35-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxCredential -ResourceId "/subscriptions/fa68082f-8ff7-4a25-95c7-ce9da541242f/resourceGroups/TestRg1/providers/Microsoft.DataBox/jobs/TestJob1"

JobName     JobSecrets
-------     ----------
TestJob1    Microsoft.Azure.Management.DataBox.Models.DataboxJobSecrets
```

<span data-ttu-id="a5a35-114">Isso reajusta os JobSecsecsecs do trabalho especificado</span><span class="sxs-lookup"><span data-stu-id="a5a35-114">This retuns the JobSecrets of the specified job</span></span>

## <span data-ttu-id="a5a35-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a5a35-115">PARAMETERS</span></span>

### <span data-ttu-id="a5a35-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5a35-116">-DefaultProfile</span></span>
<span data-ttu-id="a5a35-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a5a35-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5a35-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="a5a35-118">-Name</span></span>
<span data-ttu-id="a5a35-119">Nome do trabalho da Caixa de Dados</span><span class="sxs-lookup"><span data-stu-id="a5a35-119">Databox Job Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a35-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5a35-120">-ResourceGroupName</span></span>
<span data-ttu-id="a5a35-121">Nome do grupo de recursos de trabalho da caixa de dados</span><span class="sxs-lookup"><span data-stu-id="a5a35-121">Databox Job Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a35-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a5a35-122">-ResourceId</span></span>
<span data-ttu-id="a5a35-123">ID do Recurso de Trabalho da Caixa de Dados</span><span class="sxs-lookup"><span data-stu-id="a5a35-123">Databox Job Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5a35-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5a35-124">CommonParameters</span></span>
<span data-ttu-id="a5a35-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5a35-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5a35-126">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a5a35-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5a35-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="a5a35-127">INPUTS</span></span>

### <span data-ttu-id="a5a35-128">System.String</span><span class="sxs-lookup"><span data-stu-id="a5a35-128">System.String</span></span>

## <span data-ttu-id="a5a35-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="a5a35-129">OUTPUTS</span></span>

### <span data-ttu-id="a5a35-130">System.Collections.Generic.IEnumerable'1[[Microsoft.Azure.Management.DataBox.Models.UnencryptedCredentials, Microsoft.Azure.Management.DataBox, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="a5a35-130">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Management.DataBox.Models.UnencryptedCredentials, Microsoft.Azure.Management.DataBox, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="a5a35-131">Notas</span><span class="sxs-lookup"><span data-stu-id="a5a35-131">NOTES</span></span>

## <span data-ttu-id="a5a35-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a5a35-132">RELATED LINKS</span></span>
