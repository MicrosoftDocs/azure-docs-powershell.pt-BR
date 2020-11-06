---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Azure.AnalysisServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Add-AzureAnalysisServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Add-AzureAnalysisServicesAccount.md
ms.openlocfilehash: 8b5133e62139fca02dc59f84e5fb714d2a35e675
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93611014"
---
# <span data-ttu-id="afd0b-101">Add-AzureAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="afd0b-101">Add-AzureAnalysisServicesAccount</span></span>

## <span data-ttu-id="afd0b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="afd0b-102">SYNOPSIS</span></span>
<span data-ttu-id="afd0b-103">Adiciona uma conta autenticada para usar nas solicitações do cmdlet do servidor do Azure Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="afd0b-103">Adds an authenticated account to use for Azure Analysis Services server cmdlet requests.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="afd0b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="afd0b-104">SYNTAX</span></span>

### <span data-ttu-id="afd0b-105">UserParameterSetName (padrão)</span><span class="sxs-lookup"><span data-stu-id="afd0b-105">UserParameterSetName (Default)</span></span>
```
Add-AzureAnalysisServicesAccount [[-RolloutEnvironment] <String>] [[-Credential] <PSCredential>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afd0b-106">ServicePrincipalWithPasswordParameterSetName</span><span class="sxs-lookup"><span data-stu-id="afd0b-106">ServicePrincipalWithPasswordParameterSetName</span></span>
```
Add-AzureAnalysisServicesAccount [-RolloutEnvironment] <String> [-Credential] <PSCredential>
 [-ServicePrincipal] -TenantId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afd0b-107">ServicePrincipalWithCertificateParameterSetName</span><span class="sxs-lookup"><span data-stu-id="afd0b-107">ServicePrincipalWithCertificateParameterSetName</span></span>
```
Add-AzureAnalysisServicesAccount [-RolloutEnvironment] <String> [-ServicePrincipal] -TenantId <String>
 -ApplicationId <String> -CertificateThumbprint <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="afd0b-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="afd0b-108">DESCRIPTION</span></span>
<span data-ttu-id="afd0b-109">O cmdlet Add-AzureAnalysisServicesAccount é usado para fazer logon em uma instância do servidor do Azure Analysis Services</span><span class="sxs-lookup"><span data-stu-id="afd0b-109">The Add-AzureAnalysisServicesAccount cmdlet is used to login to an instance of Azure Analysis Services server</span></span>

## <span data-ttu-id="afd0b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="afd0b-110">EXAMPLES</span></span>

### <span data-ttu-id="afd0b-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="afd0b-111">Example 1</span></span>
```
PS C:\>Add-AzureAnalysisServicesAccount
RolloutEnvironment: westcentralus.asazure.windows.net
Credential: $UserCredential
```

<span data-ttu-id="afd0b-112">Este exemplo adicionará a conta especificada pela variável $UserCredential ao ambiente do westcentralus.asazure.windows.net Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="afd0b-112">This example will add the account specified by the $UserCredential variable to the westcentralus.asazure.windows.net Analysis Services environment.</span></span>

### <span data-ttu-id="afd0b-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="afd0b-113">Example 2</span></span>
```
PS C:\>$ApplicationCredential = Get-Credential
PS C:\>Add-AzureAnalysisServicesAccount -RolloutEnvironment 'westcentralus.asazure.windows.net' -ServicePrincipal -Credential $ApplicationCredential -TenantId "xxxx-xxxx-xxxx-xxxx"
```

<span data-ttu-id="afd0b-114">O primeiro comando obtém as credenciais da entidade de serviço do aplicativo e, em seguida, as armazena na variável $ApplicationCredential.</span><span class="sxs-lookup"><span data-stu-id="afd0b-114">The first command gets the application service principal credentials, and then stores them in the $ApplicationCredential variable.</span></span>
<span data-ttu-id="afd0b-115">O segundo comando adiciona a conta de entidade de serviço do aplicativo especificada pela variável $ApplicationCredential e Tenantid ao ambiente do westcentralus.asazure.windows.net Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="afd0b-115">The second command add the application service principal account specified by the $ApplicationCredential variable and TenantId to the westcentralus.asazure.windows.net Analysis Services environment.</span></span>

### <span data-ttu-id="afd0b-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="afd0b-116">Example 3</span></span>
```
PS C:\>Add-AzureAnalysisServicesAccount -RolloutEnvironment 'westcentralus.asazure.windows.net' -ServicePrincipal -ApplicationId "yyyy-yyyy-yyyy-yyyy" -CertificateThumbprint 'zzzzzzzzzzzzzzzz' -TenantId "xxxx-xxxx-xxxx-xxxx"
```

<span data-ttu-id="afd0b-117">Este exemplo adicionará a conta da entidade de serviço do aplicativo especificada pela ApplicationId, Tenantid e CertificateThumbprint ao ambiente do westcentralus.asazure.windows.net Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="afd0b-117">This example will add the application service principal account specified by the ApplicationId, TenantId and CertificateThumbprint to the westcentralus.asazure.windows.net Analysis Services environment.</span></span>

## <span data-ttu-id="afd0b-118">OS</span><span class="sxs-lookup"><span data-stu-id="afd0b-118">PARAMETERS</span></span>

### <span data-ttu-id="afd0b-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="afd0b-119">-ApplicationId</span></span>
<span data-ttu-id="afd0b-120">A ID do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="afd0b-120">The application ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ServicePrincipalWithCertificateParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afd0b-121">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="afd0b-121">-CertificateThumbprint</span></span>
<span data-ttu-id="afd0b-122">Hash do certificado (impressão digital)</span><span class="sxs-lookup"><span data-stu-id="afd0b-122">Certificate Hash (Thumbprint)</span></span>

```yaml
Type: System.String
Parameter Sets: ServicePrincipalWithCertificateParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afd0b-123">-Credential</span><span class="sxs-lookup"><span data-stu-id="afd0b-123">-Credential</span></span>
<span data-ttu-id="afd0b-124">Credenciais de logon</span><span class="sxs-lookup"><span data-stu-id="afd0b-124">Login credentials</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: UserParameterSetName
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: ServicePrincipalWithPasswordParameterSetName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afd0b-125">-RolloutEnvironment</span><span class="sxs-lookup"><span data-stu-id="afd0b-125">-RolloutEnvironment</span></span>
<span data-ttu-id="afd0b-126">Nome do ambiente do Azure Analysis Services no qual fazer logon.</span><span class="sxs-lookup"><span data-stu-id="afd0b-126">Name of the Azure Analysis Services environment to which to logon to.</span></span> <span data-ttu-id="afd0b-127">Considerando o nome completo do servidor por exemplo, asazure://westcentralus.asazure.windows.net/testserver, o valor correto para essa variável será westcentralus.asazure.windows.net</span><span class="sxs-lookup"><span data-stu-id="afd0b-127">Given the full name of the server for example asazure://westcentralus.asazure.windows.net/testserver , the correct value for this variable will be westcentralus.asazure.windows.net</span></span>

```yaml
Type: System.String
Parameter Sets: UserParameterSetName
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ServicePrincipalWithPasswordParameterSetName, ServicePrincipalWithCertificateParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afd0b-128">-UserPrincipal</span><span class="sxs-lookup"><span data-stu-id="afd0b-128">-ServicePrincipal</span></span>
<span data-ttu-id="afd0b-129">Indica que essa conta é autenticada fornecendo as credenciais de entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="afd0b-129">Indicates that this account authenticates by providing service principal credentials.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServicePrincipalWithPasswordParameterSetName, ServicePrincipalWithCertificateParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afd0b-130">-Tenantid</span><span class="sxs-lookup"><span data-stu-id="afd0b-130">-TenantId</span></span>
<span data-ttu-id="afd0b-131">Nome ou ID do locatário</span><span class="sxs-lookup"><span data-stu-id="afd0b-131">Tenant name or ID</span></span>

```yaml
Type: System.String
Parameter Sets: ServicePrincipalWithPasswordParameterSetName, ServicePrincipalWithCertificateParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afd0b-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="afd0b-132">-Confirm</span></span>
<span data-ttu-id="afd0b-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="afd0b-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afd0b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afd0b-134">-WhatIf</span></span>
<span data-ttu-id="afd0b-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="afd0b-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="afd0b-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="afd0b-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afd0b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afd0b-137">CommonParameters</span></span>
<span data-ttu-id="afd0b-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afd0b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afd0b-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="afd0b-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afd0b-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="afd0b-140">INPUTS</span></span>

## <span data-ttu-id="afd0b-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="afd0b-141">OUTPUTS</span></span>

### <span data-ttu-id="afd0b-142">Microsoft. Azure. Commands. AnalysisServices. Dataplan. AsAzureProfile</span><span class="sxs-lookup"><span data-stu-id="afd0b-142">Microsoft.Azure.Commands.AnalysisServices.Dataplane.AsAzureProfile</span></span>

## <span data-ttu-id="afd0b-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="afd0b-143">NOTES</span></span>
<span data-ttu-id="afd0b-144">Alias: Login-AzureAsAccount</span><span class="sxs-lookup"><span data-stu-id="afd0b-144">Alias: Login-AzureAsAccount</span></span>

## <span data-ttu-id="afd0b-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="afd0b-145">RELATED LINKS</span></span>

