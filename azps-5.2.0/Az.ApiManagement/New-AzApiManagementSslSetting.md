---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsslsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
ms.openlocfilehash: ea18df702913cd2ec7404a3fccb110f85e12ee47
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262046"
---
# <span data-ttu-id="378f6-101">New-AzApiManagementSslSetting</span><span class="sxs-lookup"><span data-stu-id="378f6-101">New-AzApiManagementSslSetting</span></span>

## <span data-ttu-id="378f6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="378f6-102">SYNOPSIS</span></span>
<span data-ttu-id="378f6-103">Cria uma instância de PsApiManagementSslSetting</span><span class="sxs-lookup"><span data-stu-id="378f6-103">Creates an instance of PsApiManagementSslSetting</span></span>

## <span data-ttu-id="378f6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="378f6-104">SYNTAX</span></span>

```
New-AzApiManagementSslSetting [-FrontendProtocol <Hashtable>] [-BackendProtocol <Hashtable>]
 [-CipherSuite <Hashtable>] [-ServerProtocol <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="378f6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="378f6-105">DESCRIPTION</span></span>
<span data-ttu-id="378f6-106">Comando auxiliar para criar uma instância de PsApiManagementSslSetting.</span><span class="sxs-lookup"><span data-stu-id="378f6-106">Helper command to create an instance of PsApiManagementSslSetting.</span></span>
<span data-ttu-id="378f6-107">Esse comando deve ser usado com o comando New-AzApiManagement.</span><span class="sxs-lookup"><span data-stu-id="378f6-107">This command is to be used with New-AzApiManagement command.</span></span>

## <span data-ttu-id="378f6-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="378f6-108">EXAMPLES</span></span>

### <span data-ttu-id="378f6-109">Exemplo 1: criar uma configuração SSL para habilitar o TLS 1,0 em backend e front-end</span><span class="sxs-lookup"><span data-stu-id="378f6-109">Example 1: Create an SSL Setting to enable TLS 1.0 on both Backend and Frontend</span></span>
```powershell
PS D:\github\azure-powershell\artifacts\Debug\Az.ApiManagement> $enableTls=@{"Tls10" = "True"}
PS D:\github\azure-powershell\artifacts\Debug\Az.ApiManagement> New-AzApiManagementSslSetting -FrontendProtocol $enableTls -BackendProtocol $enableTls

FrontendProtocols BackendProtocols CipherSuites ServerProtocols
----------------- ---------------- ------------ ---------------
{Tls10}           {Tls10}
```

<span data-ttu-id="378f6-110">Crie uma nova instância de PsApiManagementSslSetting para habilitar o TLSv 1,0 em ambos os front-end (entre cliente e APIM) e back-end (entre APIM e back-end) do gateway do ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="378f6-110">Create an new instance of PsApiManagementSslSetting to Enable TLSv 1.0 in both Frontend (between client and APIM) and Backend (between APIM and Backend) of ApiManagement Gateway.</span></span>

## <span data-ttu-id="378f6-111">OS</span><span class="sxs-lookup"><span data-stu-id="378f6-111">PARAMETERS</span></span>

### <span data-ttu-id="378f6-112">-BackendProtocol</span><span class="sxs-lookup"><span data-stu-id="378f6-112">-BackendProtocol</span></span>
<span data-ttu-id="378f6-113">Configurações do protocolo de segurança back-end.</span><span class="sxs-lookup"><span data-stu-id="378f6-113">Backend Security protocol settings.</span></span> <span data-ttu-id="378f6-114">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="378f6-114">This parameter is optional.</span></span>
<span data-ttu-id="378f6-115">As configurações de protocolo válidas são `Tls11` -tls 1,1 `Tls10` -TLS 1,0 `Ssl30` -SSL 3,0</span><span class="sxs-lookup"><span data-stu-id="378f6-115">The valid Protocol Settings are `Tls11` - Tls 1.1 `Tls10` - Tls 1.0 `Ssl30` - SSL 3.0</span></span>

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

### <span data-ttu-id="378f6-116">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="378f6-116">-CipherSuite</span></span>
<span data-ttu-id="378f6-117">Configurações de pacotes de codificação SSL na ordem especificada.</span><span class="sxs-lookup"><span data-stu-id="378f6-117">Ssl cipher suites settings in the specified order.</span></span> <span data-ttu-id="378f6-118">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="378f6-118">This parameter is optional.</span></span>
<span data-ttu-id="378f6-119">As configurações válidas são `TripleDes168` -habilitar/desabilitar a viagem Des 168</span><span class="sxs-lookup"><span data-stu-id="378f6-119">The valid Settings are `TripleDes168` - Enable / Disable Tripe Des 168</span></span>

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

### <span data-ttu-id="378f6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="378f6-120">-DefaultProfile</span></span>
<span data-ttu-id="378f6-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="378f6-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="378f6-122">-FrontendProtocol</span><span class="sxs-lookup"><span data-stu-id="378f6-122">-FrontendProtocol</span></span>
<span data-ttu-id="378f6-123">Configurações de protocolos de segurança de front-end.</span><span class="sxs-lookup"><span data-stu-id="378f6-123">Frontend Security protocols settings.</span></span> <span data-ttu-id="378f6-124">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="378f6-124">This parameter is optional.</span></span>
<span data-ttu-id="378f6-125">As configurações de protocolo válidas são `Tls11` -tls 1,1 `Tls10` -TLS 1,0 `Ssl30` -SSL 3,0</span><span class="sxs-lookup"><span data-stu-id="378f6-125">The valid Protocol Settings are `Tls11` - Tls 1.1 `Tls10` - Tls 1.0 `Ssl30` - SSL 3.0</span></span>


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

### <span data-ttu-id="378f6-126">-ServerProtocol</span><span class="sxs-lookup"><span data-stu-id="378f6-126">-ServerProtocol</span></span>
<span data-ttu-id="378f6-127">Configurações de protocolo de servidor como Http2.</span><span class="sxs-lookup"><span data-stu-id="378f6-127">Server protocol settings like Http2.</span></span> <span data-ttu-id="378f6-128">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="378f6-128">This parameter is optional.</span></span>
<span data-ttu-id="378f6-129">As configurações válidas são `Http2` -habilitar Http 2,0</span><span class="sxs-lookup"><span data-stu-id="378f6-129">The valid Settings are `Http2` - Enable Http 2.0</span></span>

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

### <span data-ttu-id="378f6-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="378f6-130">CommonParameters</span></span>
<span data-ttu-id="378f6-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="378f6-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="378f6-132">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="378f6-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="378f6-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="378f6-133">INPUTS</span></span>

### <span data-ttu-id="378f6-134">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="378f6-134">None</span></span>

## <span data-ttu-id="378f6-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="378f6-135">OUTPUTS</span></span>

### <span data-ttu-id="378f6-136">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementSslSettings</span><span class="sxs-lookup"><span data-stu-id="378f6-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSettings</span></span>

## <span data-ttu-id="378f6-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="378f6-137">NOTES</span></span>

## <span data-ttu-id="378f6-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="378f6-138">RELATED LINKS</span></span>

[<span data-ttu-id="378f6-139">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="378f6-139">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

