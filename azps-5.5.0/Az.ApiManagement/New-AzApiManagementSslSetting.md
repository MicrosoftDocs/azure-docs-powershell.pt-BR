---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsslsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
ms.openlocfilehash: ea18df702913cd2ec7404a3fccb110f85e12ee47
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127174"
---
# <span data-ttu-id="ca7bb-101">New-AzApiManagementSslSetting</span><span class="sxs-lookup"><span data-stu-id="ca7bb-101">New-AzApiManagementSslSetting</span></span>

## <span data-ttu-id="ca7bb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ca7bb-102">SYNOPSIS</span></span>
<span data-ttu-id="ca7bb-103">Cria uma instância do PsApiManagementSslSetting</span><span class="sxs-lookup"><span data-stu-id="ca7bb-103">Creates an instance of PsApiManagementSslSetting</span></span>

## <span data-ttu-id="ca7bb-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ca7bb-104">SYNTAX</span></span>

```
New-AzApiManagementSslSetting [-FrontendProtocol <Hashtable>] [-BackendProtocol <Hashtable>]
 [-CipherSuite <Hashtable>] [-ServerProtocol <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ca7bb-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="ca7bb-105">DESCRIPTION</span></span>
<span data-ttu-id="ca7bb-106">Comando Auxiliar para criar uma instância de PsApiManagementSslSetting.</span><span class="sxs-lookup"><span data-stu-id="ca7bb-106">Helper command to create an instance of PsApiManagementSslSetting.</span></span>
<span data-ttu-id="ca7bb-107">Esse comando deve ser usado com New-AzApiManagement comando.</span><span class="sxs-lookup"><span data-stu-id="ca7bb-107">This command is to be used with New-AzApiManagement command.</span></span>

## <span data-ttu-id="ca7bb-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ca7bb-108">EXAMPLES</span></span>

### <span data-ttu-id="ca7bb-109">Exemplo 1: Criar uma Configuração SSL para habilitar o TLS 1.0 no Backend e frontend</span><span class="sxs-lookup"><span data-stu-id="ca7bb-109">Example 1: Create an SSL Setting to enable TLS 1.0 on both Backend and Frontend</span></span>
```powershell
PS D:\github\azure-powershell\artifacts\Debug\Az.ApiManagement> $enableTls=@{"Tls10" = "True"}
PS D:\github\azure-powershell\artifacts\Debug\Az.ApiManagement> New-AzApiManagementSslSetting -FrontendProtocol $enableTls -BackendProtocol $enableTls

FrontendProtocols BackendProtocols CipherSuites ServerProtocols
----------------- ---------------- ------------ ---------------
{Tls10}           {Tls10}
```

<span data-ttu-id="ca7bb-110">Crie uma nova instância do PsApiManagementSslSetting para habilitar o TLSv 1.0 no Frontend (entre cliente e APIM) e Backend (entre APIM e Backend) do ApiManagement Gateway.</span><span class="sxs-lookup"><span data-stu-id="ca7bb-110">Create an new instance of PsApiManagementSslSetting to Enable TLSv 1.0 in both Frontend (between client and APIM) and Backend (between APIM and Backend) of ApiManagement Gateway.</span></span>

## <span data-ttu-id="ca7bb-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ca7bb-111">PARAMETERS</span></span>

### <span data-ttu-id="ca7bb-112">-BackendProtocol</span><span class="sxs-lookup"><span data-stu-id="ca7bb-112">-BackendProtocol</span></span>
<span data-ttu-id="ca7bb-113">Backend Security protocol settings.</span><span class="sxs-lookup"><span data-stu-id="ca7bb-113">Backend Security protocol settings.</span></span> <span data-ttu-id="ca7bb-114">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="ca7bb-114">This parameter is optional.</span></span>
<span data-ttu-id="ca7bb-115">As Configurações de Protocolo válidas são `Tls11` - Tls 1.1 `Tls10` - Tls 1.0 `Ssl30` - SSL 3.0</span><span class="sxs-lookup"><span data-stu-id="ca7bb-115">The valid Protocol Settings are `Tls11` - Tls 1.1 `Tls10` - Tls 1.0 `Ssl30` - SSL 3.0</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca7bb-116">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="ca7bb-116">-CipherSuite</span></span>
<span data-ttu-id="ca7bb-117">Configurações de pacote de ssl de criptogramas na ordem especificada.</span><span class="sxs-lookup"><span data-stu-id="ca7bb-117">Ssl cipher suites settings in the specified order.</span></span> <span data-ttu-id="ca7bb-118">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="ca7bb-118">This parameter is optional.</span></span>
<span data-ttu-id="ca7bb-119">As Configurações válidas são `TripleDes168` - Habilitar/Desabilitar Tripe Des 168</span><span class="sxs-lookup"><span data-stu-id="ca7bb-119">The valid Settings are `TripleDes168` - Enable / Disable Tripe Des 168</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca7bb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca7bb-120">-DefaultProfile</span></span>
<span data-ttu-id="ca7bb-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ca7bb-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca7bb-122">-FrontendProtocol</span><span class="sxs-lookup"><span data-stu-id="ca7bb-122">-FrontendProtocol</span></span>
<span data-ttu-id="ca7bb-123">Configurações de protocolo de segurança frontend.</span><span class="sxs-lookup"><span data-stu-id="ca7bb-123">Frontend Security protocols settings.</span></span> <span data-ttu-id="ca7bb-124">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="ca7bb-124">This parameter is optional.</span></span>
<span data-ttu-id="ca7bb-125">As Configurações de Protocolo válidas são `Tls11` - Tls 1.1 `Tls10` - Tls 1.0 `Ssl30` - SSL 3.0</span><span class="sxs-lookup"><span data-stu-id="ca7bb-125">The valid Protocol Settings are `Tls11` - Tls 1.1 `Tls10` - Tls 1.0 `Ssl30` - SSL 3.0</span></span>


```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca7bb-126">-ServerProtocol</span><span class="sxs-lookup"><span data-stu-id="ca7bb-126">-ServerProtocol</span></span>
<span data-ttu-id="ca7bb-127">Configurações de protocolo de servidor como Http2.</span><span class="sxs-lookup"><span data-stu-id="ca7bb-127">Server protocol settings like Http2.</span></span> <span data-ttu-id="ca7bb-128">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="ca7bb-128">This parameter is optional.</span></span>
<span data-ttu-id="ca7bb-129">As configurações válidas são `Http2` - Habilitar Http 2.0</span><span class="sxs-lookup"><span data-stu-id="ca7bb-129">The valid Settings are `Http2` - Enable Http 2.0</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca7bb-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca7bb-130">CommonParameters</span></span>
<span data-ttu-id="ca7bb-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca7bb-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca7bb-132">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ca7bb-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca7bb-133">Entradas</span><span class="sxs-lookup"><span data-stu-id="ca7bb-133">INPUTS</span></span>

### <span data-ttu-id="ca7bb-134">Nenhum</span><span class="sxs-lookup"><span data-stu-id="ca7bb-134">None</span></span>

## <span data-ttu-id="ca7bb-135">Saídas</span><span class="sxs-lookup"><span data-stu-id="ca7bb-135">OUTPUTS</span></span>

### <span data-ttu-id="ca7bb-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSettings</span><span class="sxs-lookup"><span data-stu-id="ca7bb-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSettings</span></span>

## <span data-ttu-id="ca7bb-137">Notas</span><span class="sxs-lookup"><span data-stu-id="ca7bb-137">NOTES</span></span>

## <span data-ttu-id="ca7bb-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ca7bb-138">RELATED LINKS</span></span>

[<span data-ttu-id="ca7bb-139">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="ca7bb-139">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

