---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementsslsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
ms.openlocfilehash: c1bdb71dcfbc554d8d9ca1d7d09a80053a564402
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891901"
---
# <span data-ttu-id="3dd0c-101">New-AzApiManagementSslSetting</span><span class="sxs-lookup"><span data-stu-id="3dd0c-101">New-AzApiManagementSslSetting</span></span>

## <span data-ttu-id="3dd0c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3dd0c-102">SYNOPSIS</span></span>
<span data-ttu-id="3dd0c-103">Cria uma instância de PsApiManagementSslSetting</span><span class="sxs-lookup"><span data-stu-id="3dd0c-103">Creates an instance of PsApiManagementSslSetting</span></span>

## <span data-ttu-id="3dd0c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="3dd0c-104">SYNTAX</span></span>

```
New-AzApiManagementSslSetting [-FrontendProtocol <Hashtable>] [-BackendProtocol <Hashtable>]
 [-CipherSuite <Hashtable>] [-ServerProtocol <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3dd0c-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="3dd0c-105">DESCRIPTION</span></span>
<span data-ttu-id="3dd0c-106">Comando auxiliar para criar uma instância de PsApiManagementSslSetting.</span><span class="sxs-lookup"><span data-stu-id="3dd0c-106">Helper command to create an instance of PsApiManagementSslSetting.</span></span>
<span data-ttu-id="3dd0c-107">Este comando deve ser usado com New-AzApiManagement comando.</span><span class="sxs-lookup"><span data-stu-id="3dd0c-107">This command is to be used with New-AzApiManagement command.</span></span>

## <span data-ttu-id="3dd0c-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3dd0c-108">EXAMPLES</span></span>

### <span data-ttu-id="3dd0c-109">Exemplo 1: Criar uma configuração SSL para habilitar o TLS 1.0 em Backend e Frontend</span><span class="sxs-lookup"><span data-stu-id="3dd0c-109">Example 1: Create an SSL Setting to enable TLS 1.0 on both Backend and Frontend</span></span>
```powershell
PS D:\github\azure-powershell\artifacts\Debug\Az.ApiManagement> $enableTls=@{"Tls10" = "True"}
PS D:\github\azure-powershell\artifacts\Debug\Az.ApiManagement> New-AzApiManagementSslSetting -FrontendProtocol $enableTls -BackendProtocol $enableTls

FrontendProtocols BackendProtocols CipherSuites ServerProtocols
----------------- ---------------- ------------ ---------------
{Tls10}           {Tls10}
```

<span data-ttu-id="3dd0c-110">Crie uma nova instância de PsApiManagementSslSetting para Habilitar o TLSv 1.0 em Frontend (entre cliente e APIM) e Backend (entre APIM e Backend) do ApiManagement Gateway.</span><span class="sxs-lookup"><span data-stu-id="3dd0c-110">Create an new instance of PsApiManagementSslSetting to Enable TLSv 1.0 in both Frontend (between client and APIM) and Backend (between APIM and Backend) of ApiManagement Gateway.</span></span>

## <span data-ttu-id="3dd0c-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="3dd0c-111">PARAMETERS</span></span>

### <span data-ttu-id="3dd0c-112">-BackendProtocol</span><span class="sxs-lookup"><span data-stu-id="3dd0c-112">-BackendProtocol</span></span>
<span data-ttu-id="3dd0c-113">Configurações de protocolo de segurança de back-end.</span><span class="sxs-lookup"><span data-stu-id="3dd0c-113">Backend Security protocol settings.</span></span> <span data-ttu-id="3dd0c-114">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="3dd0c-114">This parameter is optional.</span></span>
<span data-ttu-id="3dd0c-115">As configurações de protocolo válidas são `Tls11` - Tls 1.1 `Tls10` - Tls 1.0 `Ssl30` - SSL 3.0</span><span class="sxs-lookup"><span data-stu-id="3dd0c-115">The valid Protocol Settings are `Tls11` - Tls 1.1 `Tls10` - Tls 1.0 `Ssl30` - SSL 3.0</span></span>

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

### <span data-ttu-id="3dd0c-116">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="3dd0c-116">-CipherSuite</span></span>
<span data-ttu-id="3dd0c-117">Configurações de pacote de codificação Ssl na ordem especificada.</span><span class="sxs-lookup"><span data-stu-id="3dd0c-117">Ssl cipher suites settings in the specified order.</span></span> <span data-ttu-id="3dd0c-118">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="3dd0c-118">This parameter is optional.</span></span>
<span data-ttu-id="3dd0c-119">As configurações válidas são `TripleDes168` - Habilitar / Desabilitar Tripe Des 168</span><span class="sxs-lookup"><span data-stu-id="3dd0c-119">The valid Settings are `TripleDes168` - Enable / Disable Tripe Des 168</span></span>

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

### <span data-ttu-id="3dd0c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dd0c-120">-DefaultProfile</span></span>
<span data-ttu-id="3dd0c-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3dd0c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3dd0c-122">-FrontendProtocol</span><span class="sxs-lookup"><span data-stu-id="3dd0c-122">-FrontendProtocol</span></span>
<span data-ttu-id="3dd0c-123">Configurações de protocolos de segurança frontend.</span><span class="sxs-lookup"><span data-stu-id="3dd0c-123">Frontend Security protocols settings.</span></span> <span data-ttu-id="3dd0c-124">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="3dd0c-124">This parameter is optional.</span></span>
<span data-ttu-id="3dd0c-125">As configurações de protocolo válidas são `Tls11` - Tls 1.1 `Tls10` - Tls 1.0 `Ssl30` - SSL 3.0</span><span class="sxs-lookup"><span data-stu-id="3dd0c-125">The valid Protocol Settings are `Tls11` - Tls 1.1 `Tls10` - Tls 1.0 `Ssl30` - SSL 3.0</span></span>


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

### <span data-ttu-id="3dd0c-126">-ServerProtocol</span><span class="sxs-lookup"><span data-stu-id="3dd0c-126">-ServerProtocol</span></span>
<span data-ttu-id="3dd0c-127">Configurações de protocolo de servidor como Http2.</span><span class="sxs-lookup"><span data-stu-id="3dd0c-127">Server protocol settings like Http2.</span></span> <span data-ttu-id="3dd0c-128">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="3dd0c-128">This parameter is optional.</span></span>
<span data-ttu-id="3dd0c-129">As configurações válidas são `Http2` - Habilitar Http 2.0</span><span class="sxs-lookup"><span data-stu-id="3dd0c-129">The valid Settings are `Http2` - Enable Http 2.0</span></span>

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

### <span data-ttu-id="3dd0c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dd0c-130">CommonParameters</span></span>
<span data-ttu-id="3dd0c-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3dd0c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dd0c-132">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3dd0c-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dd0c-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3dd0c-133">INPUTS</span></span>

### <span data-ttu-id="3dd0c-134">Nenhum</span><span class="sxs-lookup"><span data-stu-id="3dd0c-134">None</span></span>

## <span data-ttu-id="3dd0c-135">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="3dd0c-135">OUTPUTS</span></span>

### <span data-ttu-id="3dd0c-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSettings</span><span class="sxs-lookup"><span data-stu-id="3dd0c-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSettings</span></span>

## <span data-ttu-id="3dd0c-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="3dd0c-137">NOTES</span></span>

## <span data-ttu-id="3dd0c-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3dd0c-138">RELATED LINKS</span></span>

[<span data-ttu-id="3dd0c-139">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="3dd0c-139">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

